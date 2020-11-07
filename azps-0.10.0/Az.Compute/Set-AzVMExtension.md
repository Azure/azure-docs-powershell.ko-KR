---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: c8aa9660be48f5b5eb2b95343c8a11420978448d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876868"
---
# <span data-ttu-id="90d17-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="90d17-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="90d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90d17-102">SYNOPSIS</span></span>
<span data-ttu-id="90d17-103">확장 속성을 업데이트 하거나 가상 컴퓨터에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="90d17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90d17-104">SYNTAX</span></span>

### <span data-ttu-id="90d17-105">설정 (기본값)</span><span class="sxs-lookup"><span data-stu-id="90d17-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d17-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="90d17-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d17-107">설명은</span><span class="sxs-lookup"><span data-stu-id="90d17-107">DESCRIPTION</span></span>
<span data-ttu-id="90d17-108">**AzVMExtension** cmdlet은 기존 가상 컴퓨터 확장에 대 한 속성을 업데이트 하거나 가상 컴퓨터에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="90d17-109">예제의</span><span class="sxs-lookup"><span data-stu-id="90d17-109">EXAMPLES</span></span>

### <span data-ttu-id="90d17-110">예제 1: 해시 테이블을 사용 하 여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="90d17-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="90d17-111">첫 번째 두 명령은 표준 Windows PowerShell 구문을 사용 하 여 해시 테이블을 만든 다음 해당 해시 테이블을 $Settings 및 $ProtectedSettings 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="90d17-112">자세한 내용은을 입력 `Get-Help about_Hash_Tables` 하세요.</span><span class="sxs-lookup"><span data-stu-id="90d17-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="90d17-113">두 번째 명령에는 이전에 생성 하 여 변수에 저장 한 두 개의 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="90d17-114">마지막 명령은 $Settings 및 $ProtectedSettings의 내용에 따라 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터의 확장을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="90d17-115">명령은 게시자 및 확장 형식을 포함 하는 기타 필요한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="90d17-116">예제 2: 문자열을 사용 하 여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="90d17-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="90d17-117">처음 두 명령은 설정을 포함 하는 문자열을 만든 다음 $SettingsString 및 $ProtectedSettingsString 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="90d17-118">마지막 명령은 $SettingsString 및 $ProtectedSettingsString의 내용에 따라 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터의 확장을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="90d17-119">명령은 게시자 및 확장 형식을 포함 하는 기타 필요한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="90d17-120">변수</span><span class="sxs-lookup"><span data-stu-id="90d17-120">PARAMETERS</span></span>

### <span data-ttu-id="90d17-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90d17-121">-AsJob</span></span>
<span data-ttu-id="90d17-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="90d17-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d17-123">-DefaultProfile</span></span>
<span data-ttu-id="90d17-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90d17-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="90d17-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="90d17-126">이 cmdlet이 Azure 게스트 에이전트에서 새 부 버전으로 자동으로 확장을 업데이트 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="90d17-127">기본적으로이 cmdlet은 게스트 에이전트가 확장을 업데이트할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="90d17-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="90d17-128">-ExtensionType</span></span>
<span data-ttu-id="90d17-129">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-129">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="90d17-130">-ForceRerun</span></span>
<span data-ttu-id="90d17-131">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="90d17-132">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-132">The value can be any string different from the current value.</span></span>

<span data-ttu-id="90d17-133">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="90d17-134">-위치</span><span class="sxs-lookup"><span data-stu-id="90d17-134">-Location</span></span>
<span data-ttu-id="90d17-135">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="90d17-136">-이름</span><span class="sxs-lookup"><span data-stu-id="90d17-136">-Name</span></span>
<span data-ttu-id="90d17-137">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="90d17-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="90d17-138">-ProtectedSettings</span></span>
<span data-ttu-id="90d17-139">해시 테이블로 확장에 대 한 개인 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="90d17-140">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-140">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="90d17-141">-ProtectedSettingString</span></span>
<span data-ttu-id="90d17-142">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="90d17-143">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="90d17-144">-Publisher</span></span>
<span data-ttu-id="90d17-145">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="90d17-146">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-146">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d17-147">-ResourceGroupName</span></span>
<span data-ttu-id="90d17-148">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="90d17-149">-설정</span><span class="sxs-lookup"><span data-stu-id="90d17-149">-Settings</span></span>
<span data-ttu-id="90d17-150">확장에 대 한 공용 구성을 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="90d17-151">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-151">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="90d17-152">-SettingString</span></span>
<span data-ttu-id="90d17-153">확장에 대 한 공용 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="90d17-154">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d17-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="90d17-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="90d17-156">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="90d17-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="90d17-157">-VMName</span></span>
<span data-ttu-id="90d17-158">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="90d17-159">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터의 확장을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="90d17-160">-확인</span><span class="sxs-lookup"><span data-stu-id="90d17-160">-Confirm</span></span>
<span data-ttu-id="90d17-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d17-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d17-162">-WhatIf</span></span>
<span data-ttu-id="90d17-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-163">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="90d17-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d17-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d17-165">CommonParameters</span></span>
<span data-ttu-id="90d17-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d17-167">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d17-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d17-168">입력</span><span class="sxs-lookup"><span data-stu-id="90d17-168">INPUTS</span></span>

### <span data-ttu-id="90d17-169">않아야</span><span class="sxs-lookup"><span data-stu-id="90d17-169">None</span></span>
<span data-ttu-id="90d17-170">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90d17-171">출력</span><span class="sxs-lookup"><span data-stu-id="90d17-171">OUTPUTS</span></span>

### <span data-ttu-id="90d17-172">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="90d17-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="90d17-173">상속자</span><span class="sxs-lookup"><span data-stu-id="90d17-173">NOTES</span></span>

## <span data-ttu-id="90d17-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90d17-174">RELATED LINKS</span></span>

[<span data-ttu-id="90d17-175">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="90d17-175">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="90d17-176">제거-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="90d17-176">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


