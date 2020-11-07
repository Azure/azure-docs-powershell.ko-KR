---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 2a3e954d53f18cbc120c9d9acb747b3e332a5512
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880558"
---
# <span data-ttu-id="ba301-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ba301-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="ba301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba301-102">SYNOPSIS</span></span>
<span data-ttu-id="ba301-103">가상 컴퓨터에 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba301-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba301-104">SYNTAX</span></span>

### <span data-ttu-id="ba301-105">SetCustomScriptExtensionByContainerAndFileNames (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba301-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba301-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="ba301-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba301-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ba301-107">DESCRIPTION</span></span>
<span data-ttu-id="ba301-108">**AzureRmVMCustomScriptExtension** cmdlet은 가상 컴퓨터에 사용자 지정 스크립트 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="ba301-109">이 확장 기능을 통해 가상 컴퓨터에서 스크립트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="ba301-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ba301-110">EXAMPLES</span></span>

### <span data-ttu-id="ba301-111">예제 1: 사용자 지정 스크립트 추가</span><span class="sxs-lookup"><span data-stu-id="ba301-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="ba301-112">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 사용자 지정 스크립트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ba301-113">스크립트 파일은 contososcript.exe입니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="ba301-114">변수</span><span class="sxs-lookup"><span data-stu-id="ba301-114">PARAMETERS</span></span>

### <span data-ttu-id="ba301-115">-인수</span><span class="sxs-lookup"><span data-stu-id="ba301-115">-Argument</span></span>
<span data-ttu-id="ba301-116">스크립트 확장에서 스크립트에 전달 하는 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="ba301-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ba301-117">-ContainerName</span></span>
<span data-ttu-id="ba301-118">이 cmdlet이 스크립트를 저장 하는 Azure storage 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="ba301-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba301-119">-DefaultProfile</span></span>
<span data-ttu-id="ba301-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ba301-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="ba301-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="ba301-122">-FileName</span></span>
<span data-ttu-id="ba301-123">스크립트 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-123">Specifies the name of the script file.</span></span> <span data-ttu-id="ba301-124">파일이 Azure Blob 저장소에 저장 된 경우 파일 이름 값은 대/소문자를 senstive.</span><span class="sxs-lookup"><span data-stu-id="ba301-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="ba301-125">Azure 파일 저장소에 저장 된 파일의 파일 이름은 대/소문자를 senstive 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="ba301-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="ba301-126">-FileUri</span></span>
<span data-ttu-id="ba301-127">스크립트 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="ba301-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ba301-128">-ForceRerun</span></span>
<span data-ttu-id="ba301-129">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ba301-130">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="ba301-131">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ba301-132">-위치</span><span class="sxs-lookup"><span data-stu-id="ba301-132">-Location</span></span>
<span data-ttu-id="ba301-133">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ba301-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ba301-134">-Name</span></span>
<span data-ttu-id="ba301-135">사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="ba301-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba301-136">-ResourceGroupName</span></span>
<span data-ttu-id="ba301-137">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ba301-138">-실행</span><span class="sxs-lookup"><span data-stu-id="ba301-138">-Run</span></span>
<span data-ttu-id="ba301-139">스크립트를 실행 하는 데 사용할 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="ba301-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="ba301-140">-SecureExecution</span></span>
<span data-ttu-id="ba301-141">이 cmdlet이 *Run* 매개 변수의 값이 서버에 로깅되지 않았는지, 그리고 확장 API를 사용 하 여 사용자에 게 반환 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="ba301-142">*실행* 값에는 스크립트 파일에 안전 하 게 전달할 비밀 또는 암호가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="ba301-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba301-143">-StorageAccountKey</span></span>
<span data-ttu-id="ba301-144">Azure 저장소 컨테이너의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="ba301-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba301-145">-StorageAccountName</span></span>
<span data-ttu-id="ba301-146">이 cmdlet이 스크립트를 저장 하는 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="ba301-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ba301-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ba301-148">저장소 끝점 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="ba301-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ba301-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="ba301-150">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ba301-151">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzureRmVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="ba301-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="ba301-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba301-152">-VMName</span></span>
<span data-ttu-id="ba301-153">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ba301-154">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 사용자 지정 스크립트 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba301-155">-확인</span><span class="sxs-lookup"><span data-stu-id="ba301-155">-Confirm</span></span>
<span data-ttu-id="ba301-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba301-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba301-157">-WhatIf</span></span>
<span data-ttu-id="ba301-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ba301-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba301-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba301-160">CommonParameters</span></span>
<span data-ttu-id="ba301-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba301-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba301-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba301-163">입력</span><span class="sxs-lookup"><span data-stu-id="ba301-163">INPUTS</span></span>

### <span data-ttu-id="ba301-164">않아야</span><span class="sxs-lookup"><span data-stu-id="ba301-164">None</span></span>
<span data-ttu-id="ba301-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba301-166">출력</span><span class="sxs-lookup"><span data-stu-id="ba301-166">OUTPUTS</span></span>

### <span data-ttu-id="ba301-167">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ba301-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ba301-168">상속자</span><span class="sxs-lookup"><span data-stu-id="ba301-168">NOTES</span></span>

## <span data-ttu-id="ba301-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba301-169">RELATED LINKS</span></span>

[<span data-ttu-id="ba301-170">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ba301-170">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="ba301-171">제거-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ba301-171">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


