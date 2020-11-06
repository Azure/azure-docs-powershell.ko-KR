---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 4ac549e53054d0650c0e64e45c662c6b184067b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531874"
---
# <span data-ttu-id="cadae-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadae-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="cadae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadae-102">SYNOPSIS</span></span>
<span data-ttu-id="cadae-103">자동화에서 DSC 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cadae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cadae-104">SYNTAX</span></span>

### <span data-ttu-id="cadae-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="cadae-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cadae-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cadae-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cadae-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cadae-107">DESCRIPTION</span></span>
<span data-ttu-id="cadae-108">**AzureRmAutomationDscConfiguration** Cmdlet은 Azure AUTOMATION에서 Ap (원하는 상태 구성) 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="cadae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cadae-109">EXAMPLES</span></span>

### <span data-ttu-id="cadae-110">예제 1: 모든 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="cadae-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cadae-111">이 명령은 Contoso17 이라는 자동화 계정의 모든 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cadae-112">예제 2: 이름별로 DSC 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="cadae-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="cadae-113">이 명령은 Contoso17 이라는 자동화 계정에서 MyConfiguration 이라는 DSC 구성에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cadae-114">변수</span><span class="sxs-lookup"><span data-stu-id="cadae-114">PARAMETERS</span></span>

### <span data-ttu-id="cadae-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cadae-115">-AutomationAccountName</span></span>
<span data-ttu-id="cadae-116">이 cmdlet이 가져오는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cadae-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cadae-117">-Name</span></span>
<span data-ttu-id="cadae-118">이 cmdlet이 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-118">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cadae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadae-119">-ResourceGroupName</span></span>
<span data-ttu-id="cadae-120">이 cmdlet에서 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-120">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="cadae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadae-121">-DefaultProfile</span></span>
<span data-ttu-id="cadae-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cadae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadae-123">CommonParameters</span></span>
<span data-ttu-id="cadae-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadae-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadae-126">입력</span><span class="sxs-lookup"><span data-stu-id="cadae-126">INPUTS</span></span>

## <span data-ttu-id="cadae-127">출력</span><span class="sxs-lookup"><span data-stu-id="cadae-127">OUTPUTS</span></span>

### <span data-ttu-id="cadae-128">DscConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="cadae-128">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="cadae-129">상속자</span><span class="sxs-lookup"><span data-stu-id="cadae-129">NOTES</span></span>

## <span data-ttu-id="cadae-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cadae-130">RELATED LINKS</span></span>

[<span data-ttu-id="cadae-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadae-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="cadae-132">가져오기-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadae-132">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


