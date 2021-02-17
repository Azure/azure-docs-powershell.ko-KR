---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209917"
---
# <span data-ttu-id="16cf2-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="16cf2-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="16cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="16cf2-103">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="16cf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="16cf2-104">SYNTAX</span></span>

### <span data-ttu-id="16cf2-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="16cf2-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="16cf2-106">만들기</span><span class="sxs-lookup"><span data-stu-id="16cf2-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16cf2-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16cf2-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="16cf2-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16cf2-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16cf2-109">설명</span><span class="sxs-lookup"><span data-stu-id="16cf2-109">DESCRIPTION</span></span>
<span data-ttu-id="16cf2-110">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="16cf2-111">예제</span><span class="sxs-lookup"><span data-stu-id="16cf2-111">EXAMPLES</span></span>

### <span data-ttu-id="16cf2-112">예제 1: 머신에 새 확장 추가</span><span class="sxs-lookup"><span data-stu-id="16cf2-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="16cf2-113">머신에서 확장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="16cf2-114">예제 2: 파이프라인을 통해 지정된 확장 매개 변수를 사용하여 새 확장 추가</span><span class="sxs-lookup"><span data-stu-id="16cf2-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="16cf2-115">파이프라인을 통해 전달된 개체에서 제공하는 확장 매개 변수를 사용하여 새 확장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="16cf2-116">이는 한 컴퓨터의 매개 변수를 잡고 다른 머신에 적용하려는 경우 매우 좋은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="16cf2-117">예제 3: 파이프라인을 통해 지정된 위치가 있는 새 확장 추가</span><span class="sxs-lookup"><span data-stu-id="16cf2-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="16cf2-118">파이프라인을 통해 제공된 ID를 사용하여 새 컴퓨터 확장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="16cf2-119">이렇게 하지는 않지만 가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="16cf2-120">예제 4: 업데이트할 위치 및 매개 변수로 확장 개체를 사용하여 새 확장 추가</span><span class="sxs-lookup"><span data-stu-id="16cf2-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="16cf2-121">파이프라인을 통해 제공된 ID 및 전달된 확장 개체에서 제공하는 확장 세부 정보를 사용하여 새 컴퓨터 확장을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="16cf2-122">이렇게 하지는 않지만 가능할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="16cf2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16cf2-123">PARAMETERS</span></span>

### <span data-ttu-id="16cf2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16cf2-124">-AsJob</span></span>
<span data-ttu-id="16cf2-125">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="16cf2-125">Run the command as a job</span></span>

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

### <span data-ttu-id="16cf2-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="16cf2-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="16cf2-127">배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="16cf2-128">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cf2-129">-DefaultProfile</span></span>
<span data-ttu-id="16cf2-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="16cf2-131">-ExtensionParameter</span></span>
<span data-ttu-id="16cf2-132">컴퓨터 확장을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="16cf2-133">생성을 위해 EXTENSIONPARAMETER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="16cf2-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="16cf2-134">-ExtensionType</span></span>
<span data-ttu-id="16cf2-135">확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="16cf2-136">-ForceRerun</span></span>
<span data-ttu-id="16cf2-137">확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16cf2-138">-InputObject</span></span>
<span data-ttu-id="16cf2-139">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="16cf2-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-140">-Location</span><span class="sxs-lookup"><span data-stu-id="16cf2-140">-Location</span></span>
<span data-ttu-id="16cf2-141">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="16cf2-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="16cf2-142">-MachineName</span></span>
<span data-ttu-id="16cf2-143">확장을 만들거나 업데이트해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-144">-Name</span><span class="sxs-lookup"><span data-stu-id="16cf2-144">-Name</span></span>
<span data-ttu-id="16cf2-145">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="16cf2-146">-NoWait</span></span>
<span data-ttu-id="16cf2-147">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="16cf2-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="16cf2-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="16cf2-148">-ProtectedSetting</span></span>
<span data-ttu-id="16cf2-149">확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="16cf2-150">-Publisher</span></span>
<span data-ttu-id="16cf2-151">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16cf2-152">-ResourceGroupName</span></span>
<span data-ttu-id="16cf2-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-154">-Setting</span><span class="sxs-lookup"><span data-stu-id="16cf2-154">-Setting</span></span>
<span data-ttu-id="16cf2-155">확장에 대한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16cf2-156">-SubscriptionId</span></span>
<span data-ttu-id="16cf2-157">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="16cf2-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="16cf2-159">-Tag</span></span>
<span data-ttu-id="16cf2-160">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="16cf2-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="16cf2-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="16cf2-162">스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16cf2-163">-Confirm</span></span>
<span data-ttu-id="16cf2-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16cf2-165">-WhatIf</span></span>
<span data-ttu-id="16cf2-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16cf2-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16cf2-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cf2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cf2-168">CommonParameters</span></span>
<span data-ttu-id="16cf2-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cf2-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16cf2-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cf2-171">입력</span><span class="sxs-lookup"><span data-stu-id="16cf2-171">INPUTS</span></span>

### <span data-ttu-id="16cf2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="16cf2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="16cf2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="16cf2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="16cf2-174">출력</span><span class="sxs-lookup"><span data-stu-id="16cf2-174">OUTPUTS</span></span>

### <span data-ttu-id="16cf2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="16cf2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="16cf2-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16cf2-176">NOTES</span></span>

<span data-ttu-id="16cf2-177">별칭</span><span class="sxs-lookup"><span data-stu-id="16cf2-177">ALIASES</span></span>

<span data-ttu-id="16cf2-178">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="16cf2-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16cf2-179">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16cf2-180">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16cf2-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16cf2-181">EXTENSIONPARAMETER: <IMachineExtension> 컴퓨터 확장을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="16cf2-182">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="16cf2-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="16cf2-183">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="16cf2-184">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="16cf2-185">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="16cf2-186">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="16cf2-187">`[ForceUpdateTag <String>]`: 확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="16cf2-188">`[MachineExtensionType <String>]`: 확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="16cf2-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: 확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="16cf2-190">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="16cf2-191">`[Setting <IMachineExtensionPropertiesSettings>]`: 확장에 대한 Json 형식 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="16cf2-192">`[TypeHandlerVersion <String>]`: 스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="16cf2-193">INPUTOBJECT: <IConnectedMachineIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="16cf2-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16cf2-194">`[ExtensionName <String>]`: 컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="16cf2-195">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="16cf2-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16cf2-196">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="16cf2-197">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="16cf2-198">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="16cf2-199">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="16cf2-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="16cf2-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16cf2-200">RELATED LINKS</span></span>

