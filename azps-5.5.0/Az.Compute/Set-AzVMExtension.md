---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204728"
---
# <span data-ttu-id="42dfe-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="42dfe-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="42dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="42dfe-103">확장 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="42dfe-104">구문</span><span class="sxs-lookup"><span data-stu-id="42dfe-104">SYNTAX</span></span>

### <span data-ttu-id="42dfe-105">설정(기본값)</span><span class="sxs-lookup"><span data-stu-id="42dfe-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42dfe-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="42dfe-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dfe-107">설명</span><span class="sxs-lookup"><span data-stu-id="42dfe-107">DESCRIPTION</span></span>
<span data-ttu-id="42dfe-108">**Set-AzVMExtension** cmdlet은 기존 Virtual Machine 확장에 대한 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="42dfe-109">예제</span><span class="sxs-lookup"><span data-stu-id="42dfe-109">EXAMPLES</span></span>

### <span data-ttu-id="42dfe-110">예제 1: 해시 테이블을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="42dfe-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="42dfe-111">처음 두 명령은 표준 Windows PowerShell 구문을 사용하여 해시 테이블을 만든 다음 해당 해시 테이블을 $Settings 및 $ProtectedSettings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="42dfe-112">자세한 내용은 `Get-Help about_Hash_Tables` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="42dfe-113">두 번째 명령에는 이전에 만든 두 개의 값이 포함되고 변수에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="42dfe-114">마지막 명령은 ResourceGroup11에서 VirtualMachine22라는 가상 머신의 확장을 $Settings $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="42dfe-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="42dfe-115">이 명령은 게시자 및 확장 유형을 포함하는 기타 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="42dfe-116">예제 2: 문자열을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="42dfe-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="42dfe-117">처음 두 명령은 설정이 포함된 문자열을 만든 다음 $SettingsString 변수 및 $ProtectedSettingsString 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="42dfe-118">마지막 명령은 ResourceGroup11에서 VirtualMachine22라는 가상 머신의 확장을 $SettingsString $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="42dfe-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="42dfe-119">이 명령은 게시자 및 확장 유형을 포함하는 기타 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="42dfe-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42dfe-120">PARAMETERS</span></span>

### <span data-ttu-id="42dfe-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42dfe-121">-AsJob</span></span>
<span data-ttu-id="42dfe-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="42dfe-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42dfe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dfe-123">-DefaultProfile</span></span>
<span data-ttu-id="42dfe-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42dfe-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="42dfe-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="42dfe-126">이 cmdlet은 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="42dfe-127">기본적으로 이 cmdlet을 사용하면 게스트 에이전트가 확장을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="42dfe-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="42dfe-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="42dfe-129">사용 가능한 확장의 최신 버전이 있는 경우 플랫폼에서 확장을 자동으로 업그레이드해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

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

### <span data-ttu-id="42dfe-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="42dfe-130">-ExtensionType</span></span>
<span data-ttu-id="42dfe-131">확장 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-131">Specifies the extension type.</span></span>

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

### <span data-ttu-id="42dfe-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="42dfe-132">-ForceRerun</span></span>
<span data-ttu-id="42dfe-133">이 cmdlet이 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 강제로 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="42dfe-134">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="42dfe-135">forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="42dfe-136">-Location</span><span class="sxs-lookup"><span data-stu-id="42dfe-136">-Location</span></span>
<span data-ttu-id="42dfe-137">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="42dfe-138">-Name</span><span class="sxs-lookup"><span data-stu-id="42dfe-138">-Name</span></span>
<span data-ttu-id="42dfe-139">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-139">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="42dfe-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="42dfe-140">-NoWait</span></span>
<span data-ttu-id="42dfe-141">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="42dfe-142">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="42dfe-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="42dfe-143">-ProtectedSettings</span></span>
<span data-ttu-id="42dfe-144">확장에 대한 개인 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="42dfe-145">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-145">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="42dfe-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="42dfe-146">-ProtectedSettingString</span></span>
<span data-ttu-id="42dfe-147">확장에 대한 개인 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="42dfe-148">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-148">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="42dfe-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="42dfe-149">-Publisher</span></span>
<span data-ttu-id="42dfe-150">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="42dfe-151">게시자는 확장을 등록할 때 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-151">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="42dfe-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dfe-152">-ResourceGroupName</span></span>
<span data-ttu-id="42dfe-153">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-153">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42dfe-154">-Settings</span><span class="sxs-lookup"><span data-stu-id="42dfe-154">-Settings</span></span>
<span data-ttu-id="42dfe-155">확장에 대한 공용 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="42dfe-156">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-156">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="42dfe-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="42dfe-157">-SettingString</span></span>
<span data-ttu-id="42dfe-158">확장에 대한 공용 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="42dfe-159">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-159">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="42dfe-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="42dfe-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="42dfe-161">이 가상 머신에 사용할 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="42dfe-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="42dfe-162">-VMName</span></span>
<span data-ttu-id="42dfe-163">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="42dfe-164">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 확장을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="42dfe-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42dfe-165">-Confirm</span></span>
<span data-ttu-id="42dfe-166">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dfe-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dfe-167">-WhatIf</span></span>
<span data-ttu-id="42dfe-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42dfe-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dfe-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dfe-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dfe-170">CommonParameters</span></span>
<span data-ttu-id="42dfe-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dfe-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dfe-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42dfe-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dfe-173">입력</span><span class="sxs-lookup"><span data-stu-id="42dfe-173">INPUTS</span></span>

### <span data-ttu-id="42dfe-174">System.String</span><span class="sxs-lookup"><span data-stu-id="42dfe-174">System.String</span></span>

### <span data-ttu-id="42dfe-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="42dfe-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="42dfe-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42dfe-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42dfe-177">출력</span><span class="sxs-lookup"><span data-stu-id="42dfe-177">OUTPUTS</span></span>

### <span data-ttu-id="42dfe-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42dfe-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="42dfe-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42dfe-179">NOTES</span></span>

## <span data-ttu-id="42dfe-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42dfe-180">RELATED LINKS</span></span>

[<span data-ttu-id="42dfe-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="42dfe-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="42dfe-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="42dfe-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


