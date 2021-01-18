---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494324"
---
# <span data-ttu-id="78d00-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="78d00-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="78d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d00-102">SYNOPSIS</span></span>
<span data-ttu-id="78d00-103">DSC 노드 또는 Hybrid Worker를 Automation에 등록하기 위한 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="78d00-104">구문</span><span class="sxs-lookup"><span data-stu-id="78d00-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78d00-105">설명</span><span class="sxs-lookup"><span data-stu-id="78d00-105">DESCRIPTION</span></span>
<span data-ttu-id="78d00-106">**Get-AzAutomationRegistrationInfo** cmdlet은 DSC(필요한 상태 구성) 노드 또는 하이브리드 작업을 Azure Automation 계정에 온보드하는 데 필요한 엔드포인트 및 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="78d00-107">예제</span><span class="sxs-lookup"><span data-stu-id="78d00-107">EXAMPLES</span></span>

### <span data-ttu-id="78d00-108">예제 1: 등록 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="78d00-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="78d00-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 AutomationAccount01이라는 Automation 계정에 대한 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="78d00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78d00-110">PARAMETERS</span></span>

### <span data-ttu-id="78d00-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78d00-111">-AutomationAccountName</span></span>
<span data-ttu-id="78d00-112">이 cmdlet이 등록 정보를 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="78d00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d00-113">-DefaultProfile</span></span>
<span data-ttu-id="78d00-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78d00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d00-115">-ResourceGroupName</span></span>
<span data-ttu-id="78d00-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="78d00-117">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹에 대한 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78d00-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d00-118">CommonParameters</span></span>
<span data-ttu-id="78d00-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78d00-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d00-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78d00-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d00-121">입력</span><span class="sxs-lookup"><span data-stu-id="78d00-121">INPUTS</span></span>

### <span data-ttu-id="78d00-122">System.String</span><span class="sxs-lookup"><span data-stu-id="78d00-122">System.String</span></span>

## <span data-ttu-id="78d00-123">출력</span><span class="sxs-lookup"><span data-stu-id="78d00-123">OUTPUTS</span></span>

### <span data-ttu-id="78d00-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="78d00-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="78d00-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78d00-125">NOTES</span></span>

## <span data-ttu-id="78d00-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78d00-126">RELATED LINKS</span></span>

[<span data-ttu-id="78d00-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="78d00-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="78d00-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="78d00-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="78d00-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="78d00-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


