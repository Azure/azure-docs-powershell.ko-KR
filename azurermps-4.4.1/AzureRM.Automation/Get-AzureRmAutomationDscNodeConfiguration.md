---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531243"
---
# <span data-ttu-id="23433-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23433-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="23433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23433-102">SYNOPSIS</span></span>
<span data-ttu-id="23433-103">자동화에서 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23433-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23433-104">SYNTAX</span></span>

### <span data-ttu-id="23433-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="23433-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23433-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23433-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23433-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23433-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23433-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23433-108">DESCRIPTION</span></span>
<span data-ttu-id="23433-109">**AzureRmAutomationDscNodeConfiguration** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="23433-110">자동화는 DSC 노드 구성을 MOF (관리 개체 형식) 구성 문서로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="23433-111">예제의</span><span class="sxs-lookup"><span data-stu-id="23433-111">EXAMPLES</span></span>

### <span data-ttu-id="23433-112">예제 1: 모든 DSC 노드 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="23433-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="23433-113">이 명령은 Contoso17 이라는 Automation 계정의 모든 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="23433-114">예제 2: DSC 구성에 대 한 모든 DSC 노드 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="23433-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="23433-115">이 명령은 ContosoConfiguration 이라는 DSC 구성이 생성 Contoso17 이라는 자동화 계정의 모든 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="23433-116">예제 3: 이름별로 DSC 노드 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="23433-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="23433-117">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConfiguration 이름을 사용 하 여 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="23433-118">변수</span><span class="sxs-lookup"><span data-stu-id="23433-118">PARAMETERS</span></span>

### <span data-ttu-id="23433-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23433-119">-AutomationAccountName</span></span>
<span data-ttu-id="23433-120">이 cmdlet이 메타 데이터를 가져오는 DSC 노드 구성을 포함 하는 자동화 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="23433-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23433-121">-ConfigurationName</span></span>
<span data-ttu-id="23433-122">이 cmdlet이 노드 구성 메타 데이터를 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23433-123">-이름</span><span class="sxs-lookup"><span data-stu-id="23433-123">-Name</span></span>
<span data-ttu-id="23433-124">이 cmdlet에서 메타 데이터를 가져오는 DSC 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23433-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23433-125">-ResourceGroupName</span></span>
<span data-ttu-id="23433-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="23433-127">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 DSC 노드 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23433-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="23433-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="23433-128">-RollupStatus</span></span>
<span data-ttu-id="23433-129">이 cmdlet이 가져오는 DSC 노드 구성의 롤업 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="23433-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="23433-130">Valid values are:</span></span> 

- <span data-ttu-id="23433-131">잘못</span><span class="sxs-lookup"><span data-stu-id="23433-131">Bad</span></span> 
- <span data-ttu-id="23433-132">적합</span><span class="sxs-lookup"><span data-stu-id="23433-132">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23433-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23433-133">-DefaultProfile</span></span>
<span data-ttu-id="23433-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23433-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23433-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23433-135">CommonParameters</span></span>
<span data-ttu-id="23433-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23433-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23433-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23433-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23433-138">입력</span><span class="sxs-lookup"><span data-stu-id="23433-138">INPUTS</span></span>

## <span data-ttu-id="23433-139">출력</span><span class="sxs-lookup"><span data-stu-id="23433-139">OUTPUTS</span></span>

### <span data-ttu-id="23433-140">CompilationJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="23433-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="23433-141">상속자</span><span class="sxs-lookup"><span data-stu-id="23433-141">NOTES</span></span>

## <span data-ttu-id="23433-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23433-142">RELATED LINKS</span></span>

[<span data-ttu-id="23433-143">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23433-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


