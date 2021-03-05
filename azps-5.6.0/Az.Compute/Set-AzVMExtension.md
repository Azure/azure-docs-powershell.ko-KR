---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: b1c7a45f538c10c2ef6c2f03809a127a21237fc9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980859"
---
# <span data-ttu-id="ff262-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ff262-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="ff262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff262-102">SYNOPSIS</span></span>
<span data-ttu-id="ff262-103">확장 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ff262-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff262-104">SYNTAX</span></span>

### <span data-ttu-id="ff262-105">설정(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff262-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff262-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="ff262-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff262-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff262-107">DESCRIPTION</span></span>
<span data-ttu-id="ff262-108">**Set-AzVMExtension** cmdlet은 기존 Virtual Machine 확장에 대한 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ff262-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff262-109">EXAMPLES</span></span>

### <span data-ttu-id="ff262-110">예제 1: 해시 테이블을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="ff262-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="ff262-111">처음 두 명령은 표준 Windows PowerShell 구문을 사용하여 해시 테이블을 만든 다음 해당 해시 테이블을 $Settings 및 $ProtectedSettings 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="ff262-112">자세한 내용은 `Get-Help about_Hash_Tables` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="ff262-113">두 번째 명령에는 이전에 만든 두 개의 값이 변수에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="ff262-114">최종 명령은 리소스 그룹11의 VirtualMachine22라는 가상 머신의 확장을 $Settings $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ff262-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="ff262-115">이 명령은 퍼블리셔 및 확장 형식을 포함하는 기타 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="ff262-116">예제 2: 문자열을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="ff262-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="ff262-117">처음 두 명령은 설정을 포함하는 문자열을 만든 다음, $SettingsString 및 $ProtectedSettingsString 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="ff262-118">최종 명령은 리소스 그룹11의 VirtualMachine22라는 가상 머신의 확장을 $SettingsString $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ff262-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="ff262-119">이 명령은 퍼블리셔 및 확장 형식을 포함하는 기타 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="ff262-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff262-120">PARAMETERS</span></span>

### <span data-ttu-id="ff262-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff262-121">-AsJob</span></span>
<span data-ttu-id="ff262-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ff262-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff262-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff262-123">-DefaultProfile</span></span>
<span data-ttu-id="ff262-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff262-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ff262-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ff262-126">이 cmdlet을 통해 Azure 게스트 에이전트가 자동으로 확장을 최신 부 버전으로 업데이트하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="ff262-127">기본적으로 이 cmdlet을 사용하면 게스트 에이전트가 확장을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="ff262-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="ff262-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="ff262-129">사용 가능한 확장의 최신 버전이 있는 경우 플랫폼에서 확장을 자동으로 업그레이드해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ff262-130">-ExtensionType</span></span>
<span data-ttu-id="ff262-131">확장 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ff262-132">-ForceRerun</span></span>
<span data-ttu-id="ff262-133">이 cmdlet은 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 다시 억지합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ff262-134">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ff262-135">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ff262-136">-Location</span><span class="sxs-lookup"><span data-stu-id="ff262-136">-Location</span></span>
<span data-ttu-id="ff262-137">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ff262-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ff262-138">-Name</span></span>
<span data-ttu-id="ff262-139">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff262-140">-NoWait</span></span>
<span data-ttu-id="ff262-141">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ff262-142">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ff262-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="ff262-143">-ProtectedSettings</span></span>
<span data-ttu-id="ff262-144">확장에 대한 개인 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ff262-145">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="ff262-146">-ProtectedSettingString</span></span>
<span data-ttu-id="ff262-147">확장에 대한 개인 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ff262-148">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ff262-149">-Publisher</span></span>
<span data-ttu-id="ff262-150">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ff262-151">게시자는 확장을 등록할 때 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff262-152">-ResourceGroupName</span></span>
<span data-ttu-id="ff262-153">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-154">-설정</span><span class="sxs-lookup"><span data-stu-id="ff262-154">-Settings</span></span>
<span data-ttu-id="ff262-155">확장에 대한 공용 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ff262-156">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="ff262-157">-SettingString</span></span>
<span data-ttu-id="ff262-158">확장에 대한 공용 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="ff262-159">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ff262-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="ff262-161">이 가상 머신에 사용할 확장 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="ff262-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="ff262-162">-VMName</span></span>
<span data-ttu-id="ff262-163">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ff262-164">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 확장을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff262-165">-확인</span><span class="sxs-lookup"><span data-stu-id="ff262-165">-Confirm</span></span>
<span data-ttu-id="ff262-166">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff262-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff262-167">-WhatIf</span></span>
<span data-ttu-id="ff262-168">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff262-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff262-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff262-170">CommonParameters</span></span>
<span data-ttu-id="ff262-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff262-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff262-172">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff262-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff262-173">입력</span><span class="sxs-lookup"><span data-stu-id="ff262-173">INPUTS</span></span>

### <span data-ttu-id="ff262-174">System.String</span><span class="sxs-lookup"><span data-stu-id="ff262-174">System.String</span></span>

### <span data-ttu-id="ff262-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff262-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff262-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ff262-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff262-177">출력</span><span class="sxs-lookup"><span data-stu-id="ff262-177">OUTPUTS</span></span>

### <span data-ttu-id="ff262-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ff262-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ff262-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff262-179">NOTES</span></span>

## <span data-ttu-id="ff262-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff262-180">RELATED LINKS</span></span>

[<span data-ttu-id="ff262-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ff262-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="ff262-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ff262-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


