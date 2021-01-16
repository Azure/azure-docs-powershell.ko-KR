---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334238"
---
# <span data-ttu-id="50175-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="50175-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="50175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50175-102">SYNOPSIS</span></span>
<span data-ttu-id="50175-103">확장 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="50175-104">구문</span><span class="sxs-lookup"><span data-stu-id="50175-104">SYNTAX</span></span>

### <span data-ttu-id="50175-105">설정(기본값)</span><span class="sxs-lookup"><span data-stu-id="50175-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50175-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="50175-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50175-107">설명</span><span class="sxs-lookup"><span data-stu-id="50175-107">DESCRIPTION</span></span>
<span data-ttu-id="50175-108">**Set-AzVMExtension** cmdlet은 기존 Virtual Machine 확장에 대한 속성을 업데이트하거나 가상 머신에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="50175-109">예제</span><span class="sxs-lookup"><span data-stu-id="50175-109">EXAMPLES</span></span>

### <span data-ttu-id="50175-110">예제 1: 해시 테이블을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="50175-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="50175-111">처음 두 명령은 표준 Windows PowerShell 구문을 사용하여 해시 테이블을 만든 다음 해당 해시 테이블을 $Settings 및 $ProtectedSettings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="50175-112">자세한 내용은 `Get-Help about_Hash_Tables` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="50175-113">두 번째 명령에는 이전에 만들어 변수에 저장된 두 개의 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="50175-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="50175-114">마지막 명령은 ResourceGroup11에서 VirtualMachine22라는 가상 머신의 확장을 $Settings $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="50175-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="50175-115">이 명령은 게시자 및 확장 유형을 포함하는 다른 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="50175-116">예제 2: 문자열을 사용하여 설정 수정</span><span class="sxs-lookup"><span data-stu-id="50175-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="50175-117">처음 두 명령은 설정이 포함된 문자열을 만든 다음 $SettingsString 및 $ProtectedSettingsString 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="50175-118">마지막 명령은 ResourceGroup11에서 VirtualMachine22라는 가상 머신의 확장을 $SettingsString $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="50175-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="50175-119">이 명령은 게시자 및 확장 유형을 포함하는 다른 필수 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="50175-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50175-120">PARAMETERS</span></span>

### <span data-ttu-id="50175-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50175-121">-AsJob</span></span>
<span data-ttu-id="50175-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="50175-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50175-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50175-123">-DefaultProfile</span></span>
<span data-ttu-id="50175-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50175-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50175-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="50175-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="50175-126">이 cmdlet은 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="50175-127">기본적으로 이 cmdlet을 사용하면 게스트 에이전트가 확장을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50175-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="50175-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="50175-128">-ExtensionType</span></span>
<span data-ttu-id="50175-129">확장 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="50175-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="50175-130">-ForceRerun</span></span>
<span data-ttu-id="50175-131">이 cmdlet이 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 강제로 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="50175-132">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50175-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="50175-133">forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="50175-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="50175-134">-Location</span><span class="sxs-lookup"><span data-stu-id="50175-134">-Location</span></span>
<span data-ttu-id="50175-135">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="50175-136">-Name</span><span class="sxs-lookup"><span data-stu-id="50175-136">-Name</span></span>
<span data-ttu-id="50175-137">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="50175-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="50175-138">-NoWait</span></span>
<span data-ttu-id="50175-139">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="50175-140">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="50175-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="50175-141">-ProtectedSettings</span></span>
<span data-ttu-id="50175-142">확장에 대한 개인 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="50175-143">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="50175-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="50175-144">-ProtectedSettingString</span></span>
<span data-ttu-id="50175-145">확장에 대한 개인 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="50175-146">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="50175-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="50175-147">-Publisher</span></span>
<span data-ttu-id="50175-148">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="50175-149">게시자는 확장을 등록할 때 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="50175-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50175-150">-ResourceGroupName</span></span>
<span data-ttu-id="50175-151">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="50175-152">-Settings</span><span class="sxs-lookup"><span data-stu-id="50175-152">-Settings</span></span>
<span data-ttu-id="50175-153">확장에 대한 공용 구성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="50175-154">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50175-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="50175-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="50175-155">-SettingString</span></span>
<span data-ttu-id="50175-156">확장에 대한 공용 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="50175-157">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50175-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="50175-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="50175-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="50175-159">이 가상 머신에 사용할 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="50175-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="50175-160">-VMName</span></span>
<span data-ttu-id="50175-161">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="50175-162">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 확장을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="50175-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50175-163">-Confirm</span></span>
<span data-ttu-id="50175-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50175-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50175-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50175-165">-WhatIf</span></span>
<span data-ttu-id="50175-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="50175-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50175-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50175-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50175-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50175-168">CommonParameters</span></span>
<span data-ttu-id="50175-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50175-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50175-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50175-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50175-171">입력</span><span class="sxs-lookup"><span data-stu-id="50175-171">INPUTS</span></span>

### <span data-ttu-id="50175-172">System.String</span><span class="sxs-lookup"><span data-stu-id="50175-172">System.String</span></span>

### <span data-ttu-id="50175-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="50175-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50175-174">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50175-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50175-175">출력</span><span class="sxs-lookup"><span data-stu-id="50175-175">OUTPUTS</span></span>

### <span data-ttu-id="50175-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="50175-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="50175-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50175-177">NOTES</span></span>

## <span data-ttu-id="50175-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50175-178">RELATED LINKS</span></span>

[<span data-ttu-id="50175-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="50175-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="50175-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="50175-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


