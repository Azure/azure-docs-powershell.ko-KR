---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 7328eda5e6821b7c403bf949460747fbf7d215e7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880266"
---
# <span data-ttu-id="350b8-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="350b8-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="350b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="350b8-102">SYNOPSIS</span></span>
<span data-ttu-id="350b8-103">작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="350b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="350b8-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="350b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="350b8-105">DESCRIPTION</span></span>
<span data-ttu-id="350b8-106">**AzOperationalInsightsWorkspaceSharedKey** cmdlet은 작업 영역의 공유 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="350b8-107">키를 사용 하 여 Operational Insights 에이전트를 작업 영역에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="350b8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="350b8-108">EXAMPLES</span></span>

### <span data-ttu-id="350b8-109">예제 1: 작업 영역 이름으로 공유 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="350b8-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="350b8-110">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="350b8-111">예제 2: 파이프라인을 사용 하 여 공유 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="350b8-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="350b8-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져온 다음 작업 영역을 **AzOperationalInsightsWorkspaceSharedKey** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="350b8-113">명령은 해당 작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="350b8-114">변수</span><span class="sxs-lookup"><span data-stu-id="350b8-114">PARAMETERS</span></span>

### <span data-ttu-id="350b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350b8-115">-DefaultProfile</span></span>
<span data-ttu-id="350b8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="350b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="350b8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="350b8-117">-Name</span></span>
<span data-ttu-id="350b8-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="350b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="350b8-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="350b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350b8-121">CommonParameters</span></span>
<span data-ttu-id="350b8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="350b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350b8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350b8-124">입력</span><span class="sxs-lookup"><span data-stu-id="350b8-124">INPUTS</span></span>

### <span data-ttu-id="350b8-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="350b8-125">System.String</span></span>

## <span data-ttu-id="350b8-126">출력</span><span class="sxs-lookup"><span data-stu-id="350b8-126">OUTPUTS</span></span>

### <span data-ttu-id="350b8-127">OperationalInsights. PSWorkspaceKeys/.</span><span class="sxs-lookup"><span data-stu-id="350b8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="350b8-128">상속자</span><span class="sxs-lookup"><span data-stu-id="350b8-128">NOTES</span></span>

## <span data-ttu-id="350b8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="350b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="350b8-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="350b8-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="350b8-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="350b8-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

