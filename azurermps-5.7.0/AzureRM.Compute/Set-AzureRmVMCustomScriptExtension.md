---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529010"
---
# <span data-ttu-id="d6af3-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d6af3-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="d6af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6af3-102">SYNOPSIS</span></span>
<span data-ttu-id="d6af3-103">가상 컴퓨터에 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6af3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6af3-104">SYNTAX</span></span>

### <span data-ttu-id="d6af3-105">SetCustomScriptExtensionByContainerAndFileNames (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6af3-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6af3-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="d6af3-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6af3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d6af3-107">DESCRIPTION</span></span>
<span data-ttu-id="d6af3-108">**AzureRmVMCustomScriptExtension** cmdlet은 가상 컴퓨터에 사용자 지정 스크립트 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="d6af3-109">이 확장 기능을 통해 가상 컴퓨터에서 스크립트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="d6af3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6af3-110">EXAMPLES</span></span>

### <span data-ttu-id="d6af3-111">예제 1: 사용자 지정 스크립트 추가</span><span class="sxs-lookup"><span data-stu-id="d6af3-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="d6af3-112">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 사용자 지정 스크립트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d6af3-113">스크립트 파일은 contososcript.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="d6af3-114">변수</span><span class="sxs-lookup"><span data-stu-id="d6af3-114">PARAMETERS</span></span>

### <span data-ttu-id="d6af3-115">-인수</span><span class="sxs-lookup"><span data-stu-id="d6af3-115">-Argument</span></span>
<span data-ttu-id="d6af3-116">스크립트 확장에서 스크립트에 전달 하는 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-116">Specifies arguments that the script extension passes to the script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d6af3-117">-ContainerName</span></span>
<span data-ttu-id="d6af3-118">이 cmdlet이 스크립트를 저장 하는 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d6af3-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-120">-FileName</span><span class="sxs-lookup"><span data-stu-id="d6af3-120">-FileName</span></span>
<span data-ttu-id="d6af3-121">스크립트 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="d6af3-122">-FileUri</span></span>
<span data-ttu-id="d6af3-123">스크립트 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d6af3-124">-ForceRerun</span></span>
<span data-ttu-id="d6af3-125">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d6af3-126">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d6af3-127">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-128">-위치</span><span class="sxs-lookup"><span data-stu-id="d6af3-128">-Location</span></span>
<span data-ttu-id="d6af3-129">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-129">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-130">-이름</span><span class="sxs-lookup"><span data-stu-id="d6af3-130">-Name</span></span>
<span data-ttu-id="d6af3-131">사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-131">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6af3-132">-ResourceGroupName</span></span>
<span data-ttu-id="d6af3-133">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-134">-실행</span><span class="sxs-lookup"><span data-stu-id="d6af3-134">-Run</span></span>
<span data-ttu-id="d6af3-135">스크립트를 실행 하는 데 사용할 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="d6af3-136">-SecureExecution</span></span>
<span data-ttu-id="d6af3-137">이 cmdlet이 *Run* 매개 변수의 값이 서버에 로깅되지 않았는지, 그리고 확장 API를 사용 하 여 사용자에 게 반환 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="d6af3-138">*실행* 값에는 스크립트 파일에 안전 하 게 전달할 비밀 또는 암호가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6af3-139">-StorageAccountKey</span></span>
<span data-ttu-id="d6af3-140">Azure 저장소 컨테이너의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6af3-141">-StorageAccountName</span></span>
<span data-ttu-id="d6af3-142">이 cmdlet이 스크립트를 저장 하는 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d6af3-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="d6af3-144">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d6af3-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="d6af3-146">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d6af3-147">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzureRmVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="d6af3-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="d6af3-148">-VMName</span></span>
<span data-ttu-id="d6af3-149">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d6af3-150">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-151">-확인</span><span class="sxs-lookup"><span data-stu-id="d6af3-151">-Confirm</span></span>
<span data-ttu-id="d6af3-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6af3-153">-WhatIf</span></span>
<span data-ttu-id="d6af3-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d6af3-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6af3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6af3-156">CommonParameters</span></span>
<span data-ttu-id="d6af3-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6af3-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6af3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6af3-159">입력</span><span class="sxs-lookup"><span data-stu-id="d6af3-159">INPUTS</span></span>

### <span data-ttu-id="d6af3-160">않아야</span><span class="sxs-lookup"><span data-stu-id="d6af3-160">None</span></span>
<span data-ttu-id="d6af3-161">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6af3-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6af3-162">출력</span><span class="sxs-lookup"><span data-stu-id="d6af3-162">OUTPUTS</span></span>

## <span data-ttu-id="d6af3-163">상속자</span><span class="sxs-lookup"><span data-stu-id="d6af3-163">NOTES</span></span>

## <span data-ttu-id="d6af3-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6af3-164">RELATED LINKS</span></span>

[<span data-ttu-id="d6af3-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d6af3-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="d6af3-166">제거-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d6af3-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


