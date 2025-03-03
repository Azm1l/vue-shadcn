<script setup lang="ts">
import DarkMode from './DarkMode.vue';
import { Button } from './ui/button'
import {
    Sheet,
    SheetContent,
    SheetDescription,
    SheetHeader,
    SheetTitle,
    SheetTrigger,
} from '@/components/ui/sheet'

</script>

<template>
    <header class="border-b">
        <div class="container mx-auto flex h-14  items-center">
            <!--Start Desktop Navbar-->
            <div class="flex items-center mx-2 justify-between flex-1">
                <div class="flex items-center">
                    HOME
                </div>
            </div>
            <div class="hidden md:flex  items-center justify-end flex-1 gap-4">
                <p>About</p>
                <p>Services</p>
                <p>Contact Us</p>
                <DarkMode />
            </div>
            <!--End Desktop Navbar-->
            <!--Start Mobile Navbar-->
            <div class="md:hidden mx-2">
                <Sheet>
                    <SheetTrigger>Open</SheetTrigger>
                    <SheetContent>
                        <SheetHeader>
                            <SheetTitle>Are you absolutely sure?</SheetTitle>
                            <SheetDescription>
                                This action cannot be undone. This will permanently delete your account
                                and remove your data from our servers.
                            </SheetDescription>
                        </SheetHeader>
                    </SheetContent>
                </Sheet>
            </div>
        </div>
    </header>
</template>