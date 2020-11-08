---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215096"
---
# <span data-ttu-id="a5c03-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a5c03-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="a5c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c03-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c03-103">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="a5c03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5c03-104">SYNTAX</span></span>

### <span data-ttu-id="a5c03-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5c03-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c03-106">만드는</span><span class="sxs-lookup"><span data-stu-id="a5c03-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5c03-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5c03-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c03-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5c03-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5c03-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a5c03-109">DESCRIPTION</span></span>
<span data-ttu-id="a5c03-110">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="a5c03-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a5c03-111">EXAMPLES</span></span>

### <span data-ttu-id="a5c03-112">예제 1: 컴퓨터에 새 확장명 추가</span><span class="sxs-lookup"><span data-stu-id="a5c03-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="a5c03-113">컴퓨터에서 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="a5c03-114">예제 2: 파이프라인을 통해 지정 된 확장 매개 변수를 사용 하 여 새 확장명 추가</span><span class="sxs-lookup"><span data-stu-id="a5c03-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="a5c03-115">파이프라인을 통해 전달 된 개체에서 제공 하는 확장 매개 변수를 사용 하 여 새 확장명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="a5c03-116">이는 한 컴퓨터의 매개 변수를 가져와 다른 컴퓨터에 적용 하려는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="a5c03-117">예제 3: 파이프라인을 통해 지정 된 위치를 사용 하 여 새 확장명 추가</span><span class="sxs-lookup"><span data-stu-id="a5c03-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="a5c03-118">이렇게 하면 파이프라인을 통해 제공 된 id를 사용 하 여 새 컴퓨터 확장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="a5c03-119">이 작업을 수행 하지는 않지만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="a5c03-120">예제 4: 확장 개체를 사용 하 여 새 확장명 추가 업데이트를 위한 위치 및 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5c03-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="a5c03-121">이렇게 하면 파이프라인을 통해 제공 된 id를 사용 하 고 전달 된 확장 개체에서 제공 하는 확장 세부 정보로 새 컴퓨터 확장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="a5c03-122">이 작업을 수행 하지는 않지만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="a5c03-123">변수</span><span class="sxs-lookup"><span data-stu-id="a5c03-123">PARAMETERS</span></span>

### <span data-ttu-id="a5c03-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c03-124">-AsJob</span></span>
<span data-ttu-id="a5c03-125">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5c03-125">Run the command as a job</span></span>

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

### <span data-ttu-id="a5c03-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a5c03-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a5c03-127">배포 시 사용할 수 있는 확장이 새 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="a5c03-128">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="a5c03-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c03-129">-DefaultProfile</span></span>
<span data-ttu-id="a5c03-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c03-131">-ExtensionParameter 변수</span><span class="sxs-lookup"><span data-stu-id="a5c03-131">-ExtensionParameter</span></span>
<span data-ttu-id="a5c03-132">컴퓨터 확장에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="a5c03-133">생성 하려면 EXTENSIONPARAMETER 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5c03-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a5c03-134">-ExtensionType</span></span>
<span data-ttu-id="a5c03-135">확장명의 유형을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="a5c03-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a5c03-136">-ForceRerun</span></span>
<span data-ttu-id="a5c03-137">확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="a5c03-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="a5c03-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5c03-138">-InputObject</span></span>
<span data-ttu-id="a5c03-139">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5c03-140">-위치</span><span class="sxs-lookup"><span data-stu-id="a5c03-140">-Location</span></span>
<span data-ttu-id="a5c03-141">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="a5c03-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="a5c03-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="a5c03-142">-MachineName</span></span>
<span data-ttu-id="a5c03-143">확장명을 만들거나 업데이트 해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="a5c03-144">-이름</span><span class="sxs-lookup"><span data-stu-id="a5c03-144">-Name</span></span>
<span data-ttu-id="a5c03-145">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="a5c03-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5c03-146">-NoWait</span></span>
<span data-ttu-id="a5c03-147">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5c03-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5c03-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a5c03-148">-ProtectedSetting</span></span>
<span data-ttu-id="a5c03-149">확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="a5c03-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a5c03-150">-Publisher</span></span>
<span data-ttu-id="a5c03-151">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="a5c03-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c03-152">-ResourceGroupName</span></span>
<span data-ttu-id="a5c03-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5c03-154">-설정</span><span class="sxs-lookup"><span data-stu-id="a5c03-154">-Setting</span></span>
<span data-ttu-id="a5c03-155">확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="a5c03-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5c03-156">-SubscriptionId</span></span>
<span data-ttu-id="a5c03-157">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5c03-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5c03-159">태그</span><span class="sxs-lookup"><span data-stu-id="a5c03-159">-Tag</span></span>
<span data-ttu-id="a5c03-160">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="a5c03-160">Resource tags.</span></span>

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

### <span data-ttu-id="a5c03-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a5c03-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="a5c03-162">스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="a5c03-163">-확인</span><span class="sxs-lookup"><span data-stu-id="a5c03-163">-Confirm</span></span>
<span data-ttu-id="a5c03-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c03-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c03-165">-WhatIf</span></span>
<span data-ttu-id="a5c03-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c03-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c03-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c03-168">CommonParameters</span></span>
<span data-ttu-id="a5c03-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c03-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c03-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c03-171">입력</span><span class="sxs-lookup"><span data-stu-id="a5c03-171">INPUTS</span></span>

### <span data-ttu-id="a5c03-172">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5c03-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="a5c03-173">ConnectedMachine. IConnectedMachineIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5c03-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="a5c03-174">출력</span><span class="sxs-lookup"><span data-stu-id="a5c03-174">OUTPUTS</span></span>

### <span data-ttu-id="a5c03-175">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5c03-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="a5c03-176">상속자</span><span class="sxs-lookup"><span data-stu-id="a5c03-176">NOTES</span></span>

<span data-ttu-id="a5c03-177">별칭과</span><span class="sxs-lookup"><span data-stu-id="a5c03-177">ALIASES</span></span>

<span data-ttu-id="a5c03-178">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5c03-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5c03-179">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5c03-180">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c03-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5c03-181">EXTENSIONPARAMETER <IMachineExtension> : 컴퓨터 확장명을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="a5c03-182">`Location <String>`: 리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="a5c03-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="a5c03-183">`[Tag <ITrackedResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="a5c03-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a5c03-184">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a5c03-185">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="a5c03-186">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="a5c03-187">`[ForceUpdateTag <String>]`: 확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 해야 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="a5c03-188">`[MachineExtensionType <String>]`: 확장의 형식을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="a5c03-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: 확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="a5c03-190">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="a5c03-191">`[Setting <IMachineExtensionPropertiesSettings>]`: 확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="a5c03-192">`[TypeHandlerVersion <String>]`: 스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="a5c03-193">INPUTOBJECT <IConnectedMachineIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5c03-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5c03-194">`[ExtensionName <String>]`: 컴퓨터 확장명의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="a5c03-195">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a5c03-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5c03-196">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="a5c03-197">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a5c03-198">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a5c03-199">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c03-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a5c03-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5c03-200">RELATED LINKS</span></span>

