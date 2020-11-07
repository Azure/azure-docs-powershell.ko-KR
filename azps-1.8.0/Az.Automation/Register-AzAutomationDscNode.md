---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701548"
---
# <span data-ttu-id="50e48-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="50e48-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="50e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e48-102">SYNOPSIS</span></span>
<span data-ttu-id="50e48-103">Azure 가상 머신을 자동화 계정에 대 한 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="50e48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50e48-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50e48-105">DESCRIPTION</span></span>
<span data-ttu-id="50e48-106">**AzAutomationDscNode** cmdlet은 azure 가상 컴퓨터를 azure AUTOMATION 계정의 DSC (원하는 상태 구성) 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="50e48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50e48-107">EXAMPLES</span></span>

### <span data-ttu-id="50e48-108">예제 1: azure 가상 머신을 Azure DSC 노드로 등록</span><span class="sxs-lookup"><span data-stu-id="50e48-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="50e48-109">이 명령은 VirtualMachine01 이라는 Azure 가상 컴퓨터를 Contoso17 이라는 Automation 계정에서 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="50e48-110">변수</span><span class="sxs-lookup"><span data-stu-id="50e48-110">PARAMETERS</span></span>

### <span data-ttu-id="50e48-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="50e48-111">-ActionAfterReboot</span></span>
<span data-ttu-id="50e48-112">가상 컴퓨터를 다시 시작 하면 수행 되는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="50e48-113">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-113">Valid values are:</span></span> 
- <span data-ttu-id="50e48-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="50e48-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="50e48-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="50e48-115">StopConfiguration</span></span>

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

### <span data-ttu-id="50e48-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="50e48-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="50e48-117">이 DSC 노드에서 다운로드 하는 새 구성이 Azure 자동화 DSC pull 서버에서 대상 노드에 이미 있는 기존 모듈을 바꿀지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="50e48-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50e48-118">-AutomationAccountName</span></span>
<span data-ttu-id="50e48-119">이 cmdlet이 가상 컴퓨터를 등록 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="50e48-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="50e48-120">-AzureVMLocation</span></span>
<span data-ttu-id="50e48-121">Azure VM 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="50e48-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="50e48-122">-AzureVMName</span></span>
<span data-ttu-id="50e48-123">Azure 자동화 DSC를 사용 하 여 관리를 등록할 Azure 가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="50e48-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50e48-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="50e48-125">Azure VM 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="50e48-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="50e48-126">-ConfigurationMode</span></span>
<span data-ttu-id="50e48-127">DSC 구성 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="50e48-128">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-128">Valid values are:</span></span> 
- <span data-ttu-id="50e48-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="50e48-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="50e48-130">ApplyAndAutocorrect 고침</span><span class="sxs-lookup"><span data-stu-id="50e48-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="50e48-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="50e48-131">ApplyOnly</span></span>

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

### <span data-ttu-id="50e48-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="50e48-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="50e48-133">DSC의 백그라운드 응용 프로그램이 대상 노드의 현재 구성을 구현 하려고 시도 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="50e48-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e48-134">-DefaultProfile</span></span>
<span data-ttu-id="50e48-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="50e48-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50e48-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="50e48-136">-NodeConfigurationName</span></span>
<span data-ttu-id="50e48-137">Azure 자동화 DSC에서 가져오도록이 cmdlet이 가상 컴퓨터를 구성 하는 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="50e48-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="50e48-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="50e48-139">필요한 경우 가상 컴퓨터를 다시 시작할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="50e48-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="50e48-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="50e48-141">로컬 구성 관리자가 Azure 자동화 DSC pull 서버에 연결 하 여 최신 노드 구성을 다운로드 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="50e48-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e48-142">-ResourceGroupName</span></span>
<span data-ttu-id="50e48-143">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="50e48-144">이 cmdlet이 가상 컴퓨터를 등록 하는 데 사용 하는 자동화 계정이이 매개 변수에서 지정 하는 리소스 그룹에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="50e48-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e48-145">CommonParameters</span></span>
<span data-ttu-id="50e48-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e48-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e48-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e48-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e48-148">입력</span><span class="sxs-lookup"><span data-stu-id="50e48-148">INPUTS</span></span>

### <span data-ttu-id="50e48-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50e48-149">System.String</span></span>

### <span data-ttu-id="50e48-150">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="50e48-150">System.Int32</span></span>

### <span data-ttu-id="50e48-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="50e48-151">System.Boolean</span></span>

## <span data-ttu-id="50e48-152">출력</span><span class="sxs-lookup"><span data-stu-id="50e48-152">OUTPUTS</span></span>

### <span data-ttu-id="50e48-153">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="50e48-153">System.Void</span></span>

## <span data-ttu-id="50e48-154">상속자</span><span class="sxs-lookup"><span data-stu-id="50e48-154">NOTES</span></span>

## <span data-ttu-id="50e48-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50e48-155">RELATED LINKS</span></span>

[<span data-ttu-id="50e48-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="50e48-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="50e48-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="50e48-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="50e48-158">등록 취소-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="50e48-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


