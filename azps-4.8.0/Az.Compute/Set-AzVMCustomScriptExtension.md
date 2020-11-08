---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048396"
---
# <span data-ttu-id="aa4bf-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa4bf-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="aa4bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4bf-103">가상 컴퓨터에 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="aa4bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa4bf-104">SYNTAX</span></span>

### <span data-ttu-id="aa4bf-105">ByNameWithContainerAndFileNamesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa4bf-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa4bf-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4bf-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa4bf-113">설명은</span><span class="sxs-lookup"><span data-stu-id="aa4bf-113">DESCRIPTION</span></span>
<span data-ttu-id="aa4bf-114">**AzVMCustomScriptExtension** cmdlet은 가상 컴퓨터에 사용자 지정 스크립트 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="aa4bf-115">이 확장 기능을 통해 가상 컴퓨터에서 스크립트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="aa4bf-116">예제의</span><span class="sxs-lookup"><span data-stu-id="aa4bf-116">EXAMPLES</span></span>

### <span data-ttu-id="aa4bf-117">예제 1: 사용자 지정 스크립트 추가</span><span class="sxs-lookup"><span data-stu-id="aa4bf-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="aa4bf-118">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 사용자 지정 스크립트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="aa4bf-119">스크립트 파일은 contososcript.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="aa4bf-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="aa4bf-120">Example 2</span></span>

<span data-ttu-id="aa4bf-121">가상 컴퓨터에 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="aa4bf-122">생성</span><span class="sxs-lookup"><span data-stu-id="aa4bf-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="aa4bf-123">변수</span><span class="sxs-lookup"><span data-stu-id="aa4bf-123">PARAMETERS</span></span>

### <span data-ttu-id="aa4bf-124">-인수</span><span class="sxs-lookup"><span data-stu-id="aa4bf-124">-Argument</span></span>
<span data-ttu-id="aa4bf-125">스크립트 확장에서 스크립트에 전달 하는 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="aa4bf-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="aa4bf-126">-ContainerName</span></span>
<span data-ttu-id="aa4bf-127">이 cmdlet이 스크립트를 저장 하는 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="aa4bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4bf-128">-DefaultProfile</span></span>
<span data-ttu-id="aa4bf-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa4bf-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="aa4bf-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="aa4bf-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="aa4bf-131">-FileName</span></span>
<span data-ttu-id="aa4bf-132">스크립트 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-132">Specifies the name of the script file.</span></span> <span data-ttu-id="aa4bf-133">파일이 Azure Blob 저장소에 저장 된 경우 파일 이름 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="aa4bf-134">Azure 파일 저장소에 저장 된 파일의 파일 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="aa4bf-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="aa4bf-135">-FileUri</span></span>
<span data-ttu-id="aa4bf-136">스크립트 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="aa4bf-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="aa4bf-137">-ForceRerun</span></span>
<span data-ttu-id="aa4bf-138">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="aa4bf-139">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="aa4bf-140">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="aa4bf-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa4bf-141">-InputObject</span></span>
<span data-ttu-id="aa4bf-142">VM 확장 개체.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-142">VM extension object.</span></span>

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

### <span data-ttu-id="aa4bf-143">-위치</span><span class="sxs-lookup"><span data-stu-id="aa4bf-143">-Location</span></span>
<span data-ttu-id="aa4bf-144">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="aa4bf-145">-이름</span><span class="sxs-lookup"><span data-stu-id="aa4bf-145">-Name</span></span>
<span data-ttu-id="aa4bf-146">사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="aa4bf-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aa4bf-147">-NoWait</span></span>
<span data-ttu-id="aa4bf-148">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="aa4bf-149">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="aa4bf-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4bf-150">-ResourceGroupName</span></span>
<span data-ttu-id="aa4bf-151">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aa4bf-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa4bf-152">-ResourceId</span></span>
<span data-ttu-id="aa4bf-153">VM 확장 ResourceID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="aa4bf-154">-실행</span><span class="sxs-lookup"><span data-stu-id="aa4bf-154">-Run</span></span>
<span data-ttu-id="aa4bf-155">스크립트를 실행 하는 데 사용할 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="aa4bf-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="aa4bf-156">-SecureExecution</span></span>
<span data-ttu-id="aa4bf-157">이 cmdlet이 *Run* 매개 변수의 값이 서버에 로깅되지 않았는지, 그리고 확장 API를 사용 하 여 사용자에 게 반환 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="aa4bf-158">*실행* 값에는 스크립트 파일에 안전 하 게 전달할 비밀 또는 암호가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="aa4bf-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aa4bf-159">-StorageAccountKey</span></span>
<span data-ttu-id="aa4bf-160">Azure 저장소 컨테이너의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="aa4bf-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa4bf-161">-StorageAccountName</span></span>
<span data-ttu-id="aa4bf-162">이 cmdlet이 스크립트를 저장 하는 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="aa4bf-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="aa4bf-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="aa4bf-164">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="aa4bf-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="aa4bf-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="aa4bf-166">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="aa4bf-167">버전을 가져오려면 *Type* 매개 변수에 대 한 # *cername* 매개 변수 및 customscriptextension의 값을 사용 하 여 Get-AzVMExtensionImage cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="aa4bf-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa4bf-168">-VMName</span></span>
<span data-ttu-id="aa4bf-169">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="aa4bf-170">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa4bf-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="aa4bf-171">-VMObject</span></span>
<span data-ttu-id="aa4bf-172">VM 개체.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-172">VM object.</span></span>

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

### <span data-ttu-id="aa4bf-173">-확인</span><span class="sxs-lookup"><span data-stu-id="aa4bf-173">-Confirm</span></span>
<span data-ttu-id="aa4bf-174">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa4bf-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4bf-175">-WhatIf</span></span>
<span data-ttu-id="aa4bf-176">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa4bf-177">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa4bf-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4bf-178">CommonParameters</span></span>
<span data-ttu-id="aa4bf-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4bf-180">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4bf-181">입력</span><span class="sxs-lookup"><span data-stu-id="aa4bf-181">INPUTS</span></span>

### <span data-ttu-id="aa4bf-182">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa4bf-182">System.String</span></span>

### <span data-ttu-id="aa4bf-183">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="aa4bf-183">System.String[]</span></span>

### <span data-ttu-id="aa4bf-184">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa4bf-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa4bf-185">출력</span><span class="sxs-lookup"><span data-stu-id="aa4bf-185">OUTPUTS</span></span>

### <span data-ttu-id="aa4bf-186">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="aa4bf-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aa4bf-187">상속자</span><span class="sxs-lookup"><span data-stu-id="aa4bf-187">NOTES</span></span>

## <span data-ttu-id="aa4bf-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa4bf-188">RELATED LINKS</span></span>

[<span data-ttu-id="aa4bf-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa4bf-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="aa4bf-190">제거-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aa4bf-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


