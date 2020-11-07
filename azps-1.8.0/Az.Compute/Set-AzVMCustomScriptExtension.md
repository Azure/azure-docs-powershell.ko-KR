---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 331850ff03feeaf1f49bd8e6a6c8486bd9b0e95a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701234"
---
# <span data-ttu-id="d0786-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d0786-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="d0786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0786-102">SYNOPSIS</span></span>
<span data-ttu-id="d0786-103">가상 컴퓨터에 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="d0786-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0786-104">SYNTAX</span></span>

### <span data-ttu-id="d0786-105">ByNameWithContainerAndFileNamesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0786-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0786-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0786-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0786-113">설명은</span><span class="sxs-lookup"><span data-stu-id="d0786-113">DESCRIPTION</span></span>
<span data-ttu-id="d0786-114">**AzVMCustomScriptExtension** cmdlet은 가상 컴퓨터에 사용자 지정 스크립트 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="d0786-115">이 확장 기능을 통해 가상 컴퓨터에서 스크립트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="d0786-116">예제의</span><span class="sxs-lookup"><span data-stu-id="d0786-116">EXAMPLES</span></span>

### <span data-ttu-id="d0786-117">예제 1: 사용자 지정 스크립트 추가</span><span class="sxs-lookup"><span data-stu-id="d0786-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="d0786-118">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 사용자 지정 스크립트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d0786-119">스크립트 파일은 contososcript.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="d0786-120">변수</span><span class="sxs-lookup"><span data-stu-id="d0786-120">PARAMETERS</span></span>

### <span data-ttu-id="d0786-121">-인수</span><span class="sxs-lookup"><span data-stu-id="d0786-121">-Argument</span></span>
<span data-ttu-id="d0786-122">스크립트 확장에서 스크립트에 전달 하는 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="d0786-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d0786-123">-ContainerName</span></span>
<span data-ttu-id="d0786-124">이 cmdlet이 스크립트를 저장 하는 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="d0786-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0786-125">-DefaultProfile</span></span>
<span data-ttu-id="d0786-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0786-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d0786-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="d0786-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="d0786-128">-FileName</span></span>
<span data-ttu-id="d0786-129">스크립트 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-129">Specifies the name of the script file.</span></span> <span data-ttu-id="d0786-130">파일이 Azure Blob 저장소에 저장 된 경우 파일 이름 값은 대/소문자를 senstive.</span><span class="sxs-lookup"><span data-stu-id="d0786-130">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="d0786-131">Azure 파일 저장소에 저장 된 파일의 파일 이름은 대/소문자를 senstive 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-131">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="d0786-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="d0786-132">-FileUri</span></span>
<span data-ttu-id="d0786-133">스크립트 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-133">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="d0786-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d0786-134">-ForceRerun</span></span>
<span data-ttu-id="d0786-135">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d0786-136">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="d0786-137">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d0786-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0786-138">-InputObject</span></span>
<span data-ttu-id="d0786-139">VM 확장 개체.</span><span class="sxs-lookup"><span data-stu-id="d0786-139">VM extension object.</span></span>

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

### <span data-ttu-id="d0786-140">-위치</span><span class="sxs-lookup"><span data-stu-id="d0786-140">-Location</span></span>
<span data-ttu-id="d0786-141">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d0786-142">-이름</span><span class="sxs-lookup"><span data-stu-id="d0786-142">-Name</span></span>
<span data-ttu-id="d0786-143">사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-143">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="d0786-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0786-144">-ResourceGroupName</span></span>
<span data-ttu-id="d0786-145">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-145">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d0786-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0786-146">-ResourceId</span></span>
<span data-ttu-id="d0786-147">VM 확장 ResourceID입니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-147">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="d0786-148">-실행</span><span class="sxs-lookup"><span data-stu-id="d0786-148">-Run</span></span>
<span data-ttu-id="d0786-149">스크립트를 실행 하는 데 사용할 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-149">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="d0786-150">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="d0786-150">-SecureExecution</span></span>
<span data-ttu-id="d0786-151">이 cmdlet이 *Run* 매개 변수의 값이 서버에 로깅되지 않았는지, 그리고 확장 API를 사용 하 여 사용자에 게 반환 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-151">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="d0786-152">*실행* 값에는 스크립트 파일에 안전 하 게 전달할 비밀 또는 암호가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-152">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="d0786-153">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0786-153">-StorageAccountKey</span></span>
<span data-ttu-id="d0786-154">Azure 저장소 컨테이너의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-154">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="d0786-155">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d0786-155">-StorageAccountName</span></span>
<span data-ttu-id="d0786-156">이 cmdlet이 스크립트를 저장 하는 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-156">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="d0786-157">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d0786-157">-StorageEndpointSuffix</span></span>
<span data-ttu-id="d0786-158">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-158">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="d0786-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d0786-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="d0786-160">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-160">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d0786-161">버전을 가져오려면 *Type* 매개 변수에 대 한 # *cername* 매개 변수 및 customscriptextension의 값을 사용 하 여 Get-AzVMExtensionImage cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-161">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="d0786-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="d0786-162">-VMName</span></span>
<span data-ttu-id="d0786-163">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d0786-164">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-164">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0786-165">-VMObject</span><span class="sxs-lookup"><span data-stu-id="d0786-165">-VMObject</span></span>
<span data-ttu-id="d0786-166">VM 개체.</span><span class="sxs-lookup"><span data-stu-id="d0786-166">VM object.</span></span>

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

### <span data-ttu-id="d0786-167">-확인</span><span class="sxs-lookup"><span data-stu-id="d0786-167">-Confirm</span></span>
<span data-ttu-id="d0786-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0786-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0786-169">-WhatIf</span></span>
<span data-ttu-id="d0786-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0786-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0786-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0786-172">CommonParameters</span></span>
<span data-ttu-id="d0786-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0786-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0786-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0786-175">입력</span><span class="sxs-lookup"><span data-stu-id="d0786-175">INPUTS</span></span>

### <span data-ttu-id="d0786-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0786-176">System.String</span></span>

### <span data-ttu-id="d0786-177">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="d0786-177">System.String[]</span></span>

### <span data-ttu-id="d0786-178">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0786-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0786-179">출력</span><span class="sxs-lookup"><span data-stu-id="d0786-179">OUTPUTS</span></span>

### <span data-ttu-id="d0786-180">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="d0786-180">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d0786-181">상속자</span><span class="sxs-lookup"><span data-stu-id="d0786-181">NOTES</span></span>

## <span data-ttu-id="d0786-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0786-182">RELATED LINKS</span></span>

[<span data-ttu-id="d0786-183">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d0786-183">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="d0786-184">제거-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d0786-184">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


