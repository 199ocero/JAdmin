<script setup>
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import DeleteUserForm from "./Partials/DeleteUserForm.vue";
import UpdatePasswordForm from "./Partials/UpdatePasswordForm.vue";
import UpdateProfileInformationForm from "./Partials/UpdateProfileInformationForm.vue";
import { Head } from "@inertiajs/vue3";
import Box from "@/Components/Box.vue";

defineProps({
  mustVerifyEmail: Boolean,
  status: String,
});
</script>

<template>
  <Head title="Profile" />

  <AuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-gray-300 leading-tight">Profile</h2>
    </template>

    <div class="py-12">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8 space-y-6">
        <Box>
          <UpdateProfileInformationForm
            :must-verify-email="mustVerifyEmail"
            :status="status"
            class="max-w-xl"
          />
        </Box>

        <Box>
          <UpdatePasswordForm class="max-w-xl" />
        </Box>

        <Box>
          <DeleteUserForm class="max-w-xl" />
        </Box>
      </div>
    </div>
  </AuthenticatedLayout>
</template>
