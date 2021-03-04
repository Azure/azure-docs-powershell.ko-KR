---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 97f2c22d4e724d53c165e2e1e73ba27fce9290b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957552"
---
# <span data-ttu-id="1a3c1-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1a3c1-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="1a3c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3c1-103">가상 머신에 사용자 지정 스크립트 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="1a3c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a3c1-104">SYNTAX</span></span>

### <span data-ttu-id="1a3c1-105">ByNameWithContainerAndFileNamesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a3c1-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a3c1-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a3c1-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a3c1-113">설명</span><span class="sxs-lookup"><span data-stu-id="1a3c1-113">DESCRIPTION</span></span>
<span data-ttu-id="1a3c1-114">**Set-AzVMCustomScriptExtension** cmdlet은 가상 머신에 사용자 지정 스크립트 Virtual Machine 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="1a3c1-115">이 확장을 사용하면 가상 머신에서 자체 스크립트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="1a3c1-116">예제</span><span class="sxs-lookup"><span data-stu-id="1a3c1-116">EXAMPLES</span></span>

### <span data-ttu-id="1a3c1-117">예제 1: 사용자 지정 스크립트 추가</span><span class="sxs-lookup"><span data-stu-id="1a3c1-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="1a3c1-118">이 명령은 VirtualMachine07이라는 가상 머신에 사용자 지정 스크립트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1a3c1-119">스크립트 파일은 contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="1a3c1-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="1a3c1-120">Example 2</span></span>

<span data-ttu-id="1a3c1-121">가상 머신에 사용자 지정 스크립트 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="1a3c1-122">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="1a3c1-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="1a3c1-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a3c1-123">PARAMETERS</span></span>

### <span data-ttu-id="1a3c1-124">-Argument</span><span class="sxs-lookup"><span data-stu-id="1a3c1-124">-Argument</span></span>
<span data-ttu-id="1a3c1-125">스크립트 확장이 스크립트에 전달하는 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-125">Specifies arguments that the script extension passes to the script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1a3c1-126">-ContainerName</span></span>
<span data-ttu-id="1a3c1-127">이 cmdlet이 스크립트를 저장하는 Azure 저장소 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3c1-128">-DefaultProfile</span></span>
<span data-ttu-id="1a3c1-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1a3c1-130">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="1a3c1-131">-FileName</span></span>
<span data-ttu-id="1a3c1-132">스크립트 파일의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-132">Specifies the name of the script file.</span></span> <span data-ttu-id="1a3c1-133">파일이 Azure Blob Storage에 저장되는 경우 파일 이름 값은 대소문자 구분입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="1a3c1-134">Azure File Storage에 저장된 파일의 파일 이름은 대소문자 구분이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="1a3c1-135">-FileUri</span></span>
<span data-ttu-id="1a3c1-136">스크립트 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-136">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1a3c1-137">-ForceRerun</span></span>
<span data-ttu-id="1a3c1-138">이 cmdlet은 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 다시 억지합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1a3c1-139">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1a3c1-140">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a3c1-141">-InputObject</span></span>
<span data-ttu-id="1a3c1-142">VM 확장 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-142">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-143">-Location</span><span class="sxs-lookup"><span data-stu-id="1a3c1-143">-Location</span></span>
<span data-ttu-id="1a3c1-144">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-144">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-145">-Name</span><span class="sxs-lookup"><span data-stu-id="1a3c1-145">-Name</span></span>
<span data-ttu-id="1a3c1-146">사용자 지정 스크립트 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-146">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a3c1-147">-NoWait</span></span>
<span data-ttu-id="1a3c1-148">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1a3c1-149">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a3c1-150">-ResourceGroupName</span></span>
<span data-ttu-id="1a3c1-151">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a3c1-152">-ResourceId</span></span>
<span data-ttu-id="1a3c1-153">VM 확장 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-153">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-154">-Run</span><span class="sxs-lookup"><span data-stu-id="1a3c1-154">-Run</span></span>
<span data-ttu-id="1a3c1-155">스크립트를 실행하는 명령을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-155">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="1a3c1-156">-SecureExecution</span></span>
<span data-ttu-id="1a3c1-157">이 cmdlet은 *RUN* 매개 변수의 값이 서버에 기록되지 않은지 또는 GET 확장 API를 사용하여 사용자에게 반환되지 않는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="1a3c1-158">Run *값은* 스크립트 파일에 안전하게 전달할 비밀 또는 암호를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1a3c1-159">-StorageAccountKey</span></span>
<span data-ttu-id="1a3c1-160">Azure Storage 컨테이너의 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-160">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1a3c1-161">-StorageAccountName</span></span>
<span data-ttu-id="1a3c1-162">이 cmdlet이 스크립트를 저장하는 Azure Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1a3c1-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="1a3c1-164">저장소 엔드포인트 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-164">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1a3c1-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="1a3c1-166">이 가상 머신에 사용할 확장 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1a3c1-167">버전을 얻게 Get-AzVMExtensionImage Type 매개 변수에 대한 Microsoft.Compute 매개 변수  및 CustomScriptExtension 값을 사용하여 Get-AzVMExtensionImage cmdlet을 *실행합니다.*</span><span class="sxs-lookup"><span data-stu-id="1a3c1-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="1a3c1-168">-VMName</span></span>
<span data-ttu-id="1a3c1-169">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1a3c1-170">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 사용자 지정 스크립트 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="1a3c1-171">-VMObject</span></span>
<span data-ttu-id="1a3c1-172">VM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-172">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-173">-확인</span><span class="sxs-lookup"><span data-stu-id="1a3c1-173">-Confirm</span></span>
<span data-ttu-id="1a3c1-174">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a3c1-175">-WhatIf</span></span>
<span data-ttu-id="1a3c1-176">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a3c1-177">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c1-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3c1-178">CommonParameters</span></span>
<span data-ttu-id="1a3c1-179">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3c1-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3c1-180">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a3c1-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3c1-181">입력</span><span class="sxs-lookup"><span data-stu-id="1a3c1-181">INPUTS</span></span>

### <span data-ttu-id="1a3c1-182">System.String</span><span class="sxs-lookup"><span data-stu-id="1a3c1-182">System.String</span></span>

### <span data-ttu-id="1a3c1-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1a3c1-183">System.String[]</span></span>

### <span data-ttu-id="1a3c1-184">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a3c1-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a3c1-185">출력</span><span class="sxs-lookup"><span data-stu-id="1a3c1-185">OUTPUTS</span></span>

### <span data-ttu-id="1a3c1-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a3c1-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1a3c1-187">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a3c1-187">NOTES</span></span>

## <span data-ttu-id="1a3c1-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a3c1-188">RELATED LINKS</span></span>

[<span data-ttu-id="1a3c1-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1a3c1-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="1a3c1-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1a3c1-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


