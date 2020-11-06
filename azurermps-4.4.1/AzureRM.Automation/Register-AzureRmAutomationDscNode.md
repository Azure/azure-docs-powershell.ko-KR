---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 1a0fd95df118e734ed594cf1efe35eb8f8476f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531863"
---
# <span data-ttu-id="714a8-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="714a8-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="714a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="714a8-102">SYNOPSIS</span></span>
<span data-ttu-id="714a8-103">Azure 가상 머신을 자동화 계정에 대 한 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="714a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="714a8-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="714a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="714a8-105">DESCRIPTION</span></span>
<span data-ttu-id="714a8-106">**AzureRmAutomationDscNode** cmdlet은 azure 가상 컴퓨터를 azure AUTOMATION 계정의 DSC (원하는 상태 구성) 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="714a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="714a8-107">EXAMPLES</span></span>

### <span data-ttu-id="714a8-108">예제 1: azure 가상 머신을 Azure DSC 노드로 등록</span><span class="sxs-lookup"><span data-stu-id="714a8-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="714a8-109">이 명령은 VirtualMachine01 이라는 Azure 가상 컴퓨터를 Contoso17 이라는 Automation 계정에서 DSC 노드로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="714a8-110">변수</span><span class="sxs-lookup"><span data-stu-id="714a8-110">PARAMETERS</span></span>

### <span data-ttu-id="714a8-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="714a8-111">-ActionAfterReboot</span></span>
<span data-ttu-id="714a8-112">가상 컴퓨터를 다시 시작 하면 수행 되는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="714a8-113">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-113">Valid values are:</span></span> 

- <span data-ttu-id="714a8-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="714a8-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="714a8-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="714a8-115">StopConfiguration</span></span>

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

### <span data-ttu-id="714a8-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="714a8-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="714a8-117">이 DSC 노드에서 다운로드 하는 새 구성이 Azure 자동화 DSC pull 서버에서 대상 노드에 이미 있는 기존 모듈을 바꿀지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="714a8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="714a8-118">-AutomationAccountName</span></span>
<span data-ttu-id="714a8-119">이 cmdlet이 가상 컴퓨터를 등록 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="714a8-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="714a8-120">-AzureVMLocation</span></span>
<span data-ttu-id="714a8-121">이 cmdlet이 가상 컴퓨터를 등록 하는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="714a8-122">유효한 위치를 얻으려면 Get-AzureRMLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="714a8-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="714a8-123">-AzureVMName</span></span>
<span data-ttu-id="714a8-124">이 cmdlet이 관리를 위해 등록 하는 Azure 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="714a8-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="714a8-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="714a8-126">이 cmdlet이 등록 하는 Azure 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="714a8-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="714a8-127">-ConfigurationMode</span></span>
<span data-ttu-id="714a8-128">DSC 구성 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="714a8-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-129">Valid values are:</span></span> 

- <span data-ttu-id="714a8-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="714a8-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="714a8-131">ApplyAndAutocorrect 고침</span><span class="sxs-lookup"><span data-stu-id="714a8-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="714a8-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="714a8-132">ApplyOnly</span></span>

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

### <span data-ttu-id="714a8-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="714a8-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="714a8-134">DSC의 백그라운드 응용 프로그램이 대상 노드의 현재 구성을 구현 하려고 시도 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="714a8-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="714a8-135">-NodeConfigurationName</span></span>
<span data-ttu-id="714a8-136">Azure 자동화 DSC에서 가져오도록이 cmdlet이 가상 컴퓨터를 구성 하는 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-136">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="714a8-137">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="714a8-137">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="714a8-138">필요한 경우 가상 컴퓨터를 다시 시작할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-138">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="714a8-139">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="714a8-139">-RefreshFrequencyMins</span></span>
<span data-ttu-id="714a8-140">로컬 구성 관리자가 Azure 자동화 DSC pull 서버에 연결 하 여 최신 노드 구성을 다운로드 하는 빈도 (분)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-140">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="714a8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="714a8-141">-ResourceGroupName</span></span>
<span data-ttu-id="714a8-142">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="714a8-143">이 cmdlet이 가상 컴퓨터를 등록 하는 데 사용 하는 자동화 계정이이 매개 변수에서 지정 하는 리소스 그룹에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-143">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="714a8-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714a8-144">-DefaultProfile</span></span>
<span data-ttu-id="714a8-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="714a8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714a8-146">CommonParameters</span></span>
<span data-ttu-id="714a8-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="714a8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714a8-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="714a8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714a8-149">입력</span><span class="sxs-lookup"><span data-stu-id="714a8-149">INPUTS</span></span>

## <span data-ttu-id="714a8-150">출력</span><span class="sxs-lookup"><span data-stu-id="714a8-150">OUTPUTS</span></span>

## <span data-ttu-id="714a8-151">상속자</span><span class="sxs-lookup"><span data-stu-id="714a8-151">NOTES</span></span>

## <span data-ttu-id="714a8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="714a8-152">RELATED LINKS</span></span>

[<span data-ttu-id="714a8-153">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="714a8-153">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="714a8-154">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="714a8-154">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="714a8-155">등록 취소-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="714a8-155">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


