---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182164"
---
# <span data-ttu-id="282db-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="282db-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="282db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="282db-102">SYNOPSIS</span></span>
<span data-ttu-id="282db-103">Windows OS를 실행하는 Azure 가상 머신을 Automation 계정에 대한 DSC 노드로 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="282db-104">구문</span><span class="sxs-lookup"><span data-stu-id="282db-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="282db-105">설명</span><span class="sxs-lookup"><span data-stu-id="282db-105">DESCRIPTION</span></span>
<span data-ttu-id="282db-106">**Register-AzAutomationDscNode** cmdlet은 Azure Automation 계정에서 APS DSC(필요한 상태 구성) 노드로 Azure 가상 머신을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="282db-107">이 cmdlet은 계정에 대한 Automation DSC 노드로 Windows OS를 실행하는 VM만 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="282db-108">다른 구독의 자동화 계정에 노드를 등록해야 하는 경우 cmdlet이 아닌 ARM 템플릿을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="282db-109">자세한 내용은 Azure [Automation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="282db-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="282db-110">예제</span><span class="sxs-lookup"><span data-stu-id="282db-110">EXAMPLES</span></span>

### <span data-ttu-id="282db-111">예제 1: Azure DSC 노드로 Azure 가상 머신 등록</span><span class="sxs-lookup"><span data-stu-id="282db-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="282db-112">이 명령은 Contoso17이라는 Automation 계정에서 VirtualMachine01이라는 Azure 가상 머신을 DSC 노드로 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="282db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="282db-113">PARAMETERS</span></span>

### <span data-ttu-id="282db-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="282db-114">-ActionAfterReboot</span></span>
<span data-ttu-id="282db-115">가상 머신이 다시 시작된 후 수행한 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="282db-116">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="282db-116">Valid values are:</span></span> 
- <span data-ttu-id="282db-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="282db-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="282db-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="282db-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="282db-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="282db-120">이 DSC 노드가 Azure Automation DSC 끌어오기 서버에서 다운로드하는 새 구성이 대상 노드에 이미 있는 기존 모듈을 대체할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="282db-121">-AutomationAccountName</span></span>
<span data-ttu-id="282db-122">이 cmdlet이 가상 머신을 등록하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="282db-123">-AzureVMLocation</span></span>
<span data-ttu-id="282db-124">Azure VM 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="282db-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="282db-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="282db-125">-AzureVMName</span></span>
<span data-ttu-id="282db-126">Azure Automation DSC를 사용하여 관리를 등록할 Azure 가상 머신의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="282db-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="282db-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="282db-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="282db-128">Azure VM 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="282db-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="282db-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="282db-129">-ConfigurationMode</span></span>
<span data-ttu-id="282db-130">DSC 구성 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="282db-131">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="282db-131">Valid values are:</span></span> 
- <span data-ttu-id="282db-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="282db-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="282db-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="282db-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="282db-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="282db-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="282db-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="282db-136">DSC의 백그라운드 애플리케이션이 대상 노드에서 현재 구성을 구현하려고 시도하는 빈도(분)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282db-137">-DefaultProfile</span></span>
<span data-ttu-id="282db-138">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="282db-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="282db-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="282db-139">-NodeConfigurationName</span></span>
<span data-ttu-id="282db-140">이 cmdlet이 Azure Automation DSC에서 끌어오도록 가상 머신을 구성하는 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="282db-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="282db-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="282db-142">필요한 경우 가상 머신을 다시 시작할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="282db-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="282db-144">로컬 Configuration Manager가 Azure Automation DSC 끌어오기 서버에 연결하여 최신 노드 구성을 다운로드하는 빈도(분)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="282db-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="282db-145">-ResourceGroupName</span></span>
<span data-ttu-id="282db-146">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="282db-147">이 cmdlet이 가상 머신을 등록하는 Automation 계정은 이 매개 변수가 지정하는 리소스 그룹에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="282db-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282db-148">CommonParameters</span></span>
<span data-ttu-id="282db-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="282db-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282db-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="282db-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282db-151">입력</span><span class="sxs-lookup"><span data-stu-id="282db-151">INPUTS</span></span>

### <span data-ttu-id="282db-152">System.String</span><span class="sxs-lookup"><span data-stu-id="282db-152">System.String</span></span>

### <span data-ttu-id="282db-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="282db-153">System.Int32</span></span>

### <span data-ttu-id="282db-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="282db-154">System.Boolean</span></span>

## <span data-ttu-id="282db-155">출력</span><span class="sxs-lookup"><span data-stu-id="282db-155">OUTPUTS</span></span>

### <span data-ttu-id="282db-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="282db-156">System.Void</span></span>

## <span data-ttu-id="282db-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="282db-157">NOTES</span></span>

## <span data-ttu-id="282db-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="282db-158">RELATED LINKS</span></span>

[<span data-ttu-id="282db-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="282db-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="282db-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="282db-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="282db-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="282db-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


