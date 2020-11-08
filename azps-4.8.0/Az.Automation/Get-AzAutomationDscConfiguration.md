---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212652"
---
# <span data-ttu-id="76948-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="76948-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="76948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76948-102">SYNOPSIS</span></span>
<span data-ttu-id="76948-103">자동화에서 DSC 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76948-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="76948-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76948-104">SYNTAX</span></span>

### <span data-ttu-id="76948-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="76948-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76948-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="76948-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76948-107">설명은</span><span class="sxs-lookup"><span data-stu-id="76948-107">DESCRIPTION</span></span>
<span data-ttu-id="76948-108">**AzAutomationDscConfiguration** Cmdlet은 Azure AUTOMATION에서 Ap (원하는 상태 구성) 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76948-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="76948-109">예제의</span><span class="sxs-lookup"><span data-stu-id="76948-109">EXAMPLES</span></span>

### <span data-ttu-id="76948-110">예제 1: 모든 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="76948-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="76948-111">이 명령은 Contoso17 이라는 자동화 계정의 모든 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76948-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="76948-112">예제 2: 이름별로 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="76948-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="76948-113">이 명령은 Contoso17 이라는 자동화 계정에서 MyConfiguration 이라는 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76948-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="76948-114">변수</span><span class="sxs-lookup"><span data-stu-id="76948-114">PARAMETERS</span></span>

### <span data-ttu-id="76948-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76948-115">-AutomationAccountName</span></span>
<span data-ttu-id="76948-116">이 cmdlet이 가져오는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76948-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="76948-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76948-117">-DefaultProfile</span></span>
<span data-ttu-id="76948-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="76948-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76948-119">-이름</span><span class="sxs-lookup"><span data-stu-id="76948-119">-Name</span></span>
<span data-ttu-id="76948-120">이 cmdlet이 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76948-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76948-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76948-121">-ResourceGroupName</span></span>
<span data-ttu-id="76948-122">이 cmdlet에서 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76948-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="76948-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76948-123">CommonParameters</span></span>
<span data-ttu-id="76948-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76948-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76948-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76948-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76948-126">입력</span><span class="sxs-lookup"><span data-stu-id="76948-126">INPUTS</span></span>

### <span data-ttu-id="76948-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76948-127">System.String</span></span>

## <span data-ttu-id="76948-128">출력</span><span class="sxs-lookup"><span data-stu-id="76948-128">OUTPUTS</span></span>

### <span data-ttu-id="76948-129">DscConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="76948-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="76948-130">상속자</span><span class="sxs-lookup"><span data-stu-id="76948-130">NOTES</span></span>

## <span data-ttu-id="76948-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76948-131">RELATED LINKS</span></span>

[<span data-ttu-id="76948-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="76948-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="76948-133">가져오기-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="76948-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


