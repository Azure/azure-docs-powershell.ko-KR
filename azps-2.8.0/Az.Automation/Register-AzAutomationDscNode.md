---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5aec50c6203697ed21f8d475068752b35616eb52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697780"
---
# <span data-ttu-id="17ae7-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="17ae7-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="17ae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="17ae7-103">Windows OS를 실행 하는 Azure 가상 컴퓨터를 자동화 계정에 대 한 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="17ae7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17ae7-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ae7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17ae7-105">DESCRIPTION</span></span>
<span data-ttu-id="17ae7-106">**AzAutomationDscNode** cmdlet은 azure 가상 컴퓨터를 azure AUTOMATION 계정의 DSC (원하는 상태 구성) 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="17ae7-107">이 cmdlet은 Windows OS를 실행 하는 Vm을 계정에 대 한 자동화 DSC 노드로만 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="17ae7-108">다른 구독에서 자동화 계정에 노드를 등록 해야 하는 경우에는 cmdlet 대신 ARM 템플릿을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="17ae7-109">자세한 내용은 Azure 자동화 [문서](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17ae7-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="17ae7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="17ae7-110">EXAMPLES</span></span>

### <span data-ttu-id="17ae7-111">예제 1: azure 가상 머신을 Azure DSC 노드로 등록</span><span class="sxs-lookup"><span data-stu-id="17ae7-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="17ae7-112">이 명령은 VirtualMachine01 이라는 Azure 가상 컴퓨터를 Contoso17 이라는 Automation 계정에서 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17ae7-113">변수</span><span class="sxs-lookup"><span data-stu-id="17ae7-113">PARAMETERS</span></span>

### <span data-ttu-id="17ae7-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="17ae7-114">-ActionAfterReboot</span></span>
<span data-ttu-id="17ae7-115">가상 컴퓨터를 다시 시작 하면 수행 되는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="17ae7-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-116">Valid values are:</span></span> 
- <span data-ttu-id="17ae7-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="17ae7-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="17ae7-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="17ae7-118">StopConfiguration</span></span>

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

### <span data-ttu-id="17ae7-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="17ae7-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="17ae7-120">이 DSC 노드에서 다운로드 하는 새 구성이 Azure 자동화 DSC pull 서버에서 대상 노드에 이미 있는 기존 모듈을 바꿀지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="17ae7-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17ae7-121">-AutomationAccountName</span></span>
<span data-ttu-id="17ae7-122">이 cmdlet이 가상 컴퓨터를 등록 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="17ae7-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="17ae7-123">-AzureVMLocation</span></span>
<span data-ttu-id="17ae7-124">Azure VM 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="17ae7-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="17ae7-125">-AzureVMName</span></span>
<span data-ttu-id="17ae7-126">Azure 자동화 DSC를 사용 하 여 관리를 등록할 Azure 가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="17ae7-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17ae7-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="17ae7-128">Azure VM 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="17ae7-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="17ae7-129">-ConfigurationMode</span></span>
<span data-ttu-id="17ae7-130">DSC 구성 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="17ae7-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-131">Valid values are:</span></span> 
- <span data-ttu-id="17ae7-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="17ae7-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="17ae7-133">ApplyAndAutocorrect 고침</span><span class="sxs-lookup"><span data-stu-id="17ae7-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="17ae7-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="17ae7-134">ApplyOnly</span></span>

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

### <span data-ttu-id="17ae7-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="17ae7-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="17ae7-136">DSC의 백그라운드 응용 프로그램이 대상 노드의 현재 구성을 구현 하려고 시도 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="17ae7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ae7-137">-DefaultProfile</span></span>
<span data-ttu-id="17ae7-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17ae7-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17ae7-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="17ae7-139">-NodeConfigurationName</span></span>
<span data-ttu-id="17ae7-140">Azure 자동화 DSC에서 가져오도록이 cmdlet이 가상 컴퓨터를 구성 하는 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="17ae7-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="17ae7-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="17ae7-142">필요한 경우 가상 컴퓨터를 다시 시작할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="17ae7-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="17ae7-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="17ae7-144">로컬 구성 관리자가 Azure 자동화 DSC pull 서버에 연결 하 여 최신 노드 구성을 다운로드 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="17ae7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ae7-145">-ResourceGroupName</span></span>
<span data-ttu-id="17ae7-146">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="17ae7-147">이 cmdlet이 가상 컴퓨터를 등록 하는 데 사용 하는 자동화 계정이이 매개 변수에서 지정 하는 리소스 그룹에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="17ae7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ae7-148">CommonParameters</span></span>
<span data-ttu-id="17ae7-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ae7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ae7-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ae7-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ae7-151">입력</span><span class="sxs-lookup"><span data-stu-id="17ae7-151">INPUTS</span></span>

### <span data-ttu-id="17ae7-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17ae7-152">System.String</span></span>

### <span data-ttu-id="17ae7-153">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="17ae7-153">System.Int32</span></span>

### <span data-ttu-id="17ae7-154">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="17ae7-154">System.Boolean</span></span>

## <span data-ttu-id="17ae7-155">출력</span><span class="sxs-lookup"><span data-stu-id="17ae7-155">OUTPUTS</span></span>

### <span data-ttu-id="17ae7-156">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="17ae7-156">System.Void</span></span>

## <span data-ttu-id="17ae7-157">상속자</span><span class="sxs-lookup"><span data-stu-id="17ae7-157">NOTES</span></span>

## <span data-ttu-id="17ae7-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17ae7-158">RELATED LINKS</span></span>

[<span data-ttu-id="17ae7-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="17ae7-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="17ae7-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="17ae7-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="17ae7-161">등록 취소-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="17ae7-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


