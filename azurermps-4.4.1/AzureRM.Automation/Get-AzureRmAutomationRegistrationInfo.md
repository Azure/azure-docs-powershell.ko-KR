---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531228"
---
# <span data-ttu-id="7022d-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="7022d-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="7022d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7022d-102">SYNOPSIS</span></span>
<span data-ttu-id="7022d-103">온 보 딩 노드나 하이브리드 작업자에 게 자동화에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7022d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7022d-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7022d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7022d-105">DESCRIPTION</span></span>
<span data-ttu-id="7022d-106">**AzureRmAutomationRegistrationInfo** CMDLET은 DSC (원하는 상태 구성) 노드 또는 hybrid Worker를 Azure Automation 계정으로 온보드 위해 필요한 끝점과 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="7022d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7022d-107">EXAMPLES</span></span>

### <span data-ttu-id="7022d-108">예제 1: 등록 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7022d-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="7022d-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 자동화 계정에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="7022d-110">변수</span><span class="sxs-lookup"><span data-stu-id="7022d-110">PARAMETERS</span></span>

### <span data-ttu-id="7022d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7022d-111">-AutomationAccountName</span></span>
<span data-ttu-id="7022d-112">이 cmdlet이 등록 정보를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="7022d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7022d-113">-ResourceGroupName</span></span>
<span data-ttu-id="7022d-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7022d-115">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7022d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7022d-116">-DefaultProfile</span></span>
<span data-ttu-id="7022d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7022d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7022d-118">CommonParameters</span></span>
<span data-ttu-id="7022d-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7022d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7022d-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7022d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7022d-121">입력</span><span class="sxs-lookup"><span data-stu-id="7022d-121">INPUTS</span></span>

## <span data-ttu-id="7022d-122">출력</span><span class="sxs-lookup"><span data-stu-id="7022d-122">OUTPUTS</span></span>

### <span data-ttu-id="7022d-123">Microsoft Azure. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="7022d-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="7022d-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7022d-124">NOTES</span></span>

## <span data-ttu-id="7022d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7022d-125">RELATED LINKS</span></span>

[<span data-ttu-id="7022d-126">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7022d-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="7022d-127">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7022d-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="7022d-128">새로운 AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="7022d-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


