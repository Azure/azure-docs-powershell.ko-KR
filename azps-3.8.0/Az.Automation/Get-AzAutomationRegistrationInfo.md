---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042671"
---
# <span data-ttu-id="9d7ff-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="9d7ff-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="9d7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7ff-103">온 보 딩 노드나 하이브리드 작업자에 게 자동화에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="9d7ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d7ff-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7ff-106">**AzAutomationRegistrationInfo** CMDLET은 DSC (원하는 상태 구성) 노드 또는 hybrid Worker를 Azure Automation 계정으로 온보드 위해 필요한 끝점과 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="9d7ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9d7ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9d7ff-108">예제 1: 등록 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="9d7ff-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9d7ff-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 자동화 계정에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="9d7ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="9d7ff-110">PARAMETERS</span></span>

### <span data-ttu-id="9d7ff-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d7ff-111">-AutomationAccountName</span></span>
<span data-ttu-id="9d7ff-112">이 cmdlet이 등록 정보를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="9d7ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7ff-113">-DefaultProfile</span></span>
<span data-ttu-id="9d7ff-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d7ff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d7ff-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9d7ff-117">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹에 대 한 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7ff-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7ff-118">CommonParameters</span></span>
<span data-ttu-id="9d7ff-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7ff-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7ff-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7ff-121">입력</span><span class="sxs-lookup"><span data-stu-id="9d7ff-121">INPUTS</span></span>

### <span data-ttu-id="9d7ff-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9d7ff-122">System.String</span></span>

## <span data-ttu-id="9d7ff-123">출력</span><span class="sxs-lookup"><span data-stu-id="9d7ff-123">OUTPUTS</span></span>

### <span data-ttu-id="9d7ff-124">Microsoft Azure. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="9d7ff-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="9d7ff-125">상속자</span><span class="sxs-lookup"><span data-stu-id="9d7ff-125">NOTES</span></span>

## <span data-ttu-id="9d7ff-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d7ff-126">RELATED LINKS</span></span>

[<span data-ttu-id="9d7ff-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9d7ff-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="9d7ff-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9d7ff-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="9d7ff-129">새로운 AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="9d7ff-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


