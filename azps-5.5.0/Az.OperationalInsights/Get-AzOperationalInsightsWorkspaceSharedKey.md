---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189425"
---
# <span data-ttu-id="43322-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="43322-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="43322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43322-102">SYNOPSIS</span></span>
<span data-ttu-id="43322-103">작업 영역의 공유 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43322-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="43322-104">구문</span><span class="sxs-lookup"><span data-stu-id="43322-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43322-105">설명</span><span class="sxs-lookup"><span data-stu-id="43322-105">DESCRIPTION</span></span>
<span data-ttu-id="43322-106">**Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet은 작업 영역의 공유 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="43322-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="43322-107">키는 Operational Insights 에이전트를 작업 영역으로 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="43322-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="43322-108">예제</span><span class="sxs-lookup"><span data-stu-id="43322-108">EXAMPLES</span></span>

### <span data-ttu-id="43322-109">예제 1: 작업 영역 이름으로 공유 키 얻기</span><span class="sxs-lookup"><span data-stu-id="43322-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="43322-110">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 MyWorkspace라는 작업 영역의 공유 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43322-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="43322-111">예제 2: 파이프라인을 사용하여 공유 키 얻기</span><span class="sxs-lookup"><span data-stu-id="43322-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="43322-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역과 작업 영역이 **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="43322-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="43322-113">이 명령은 작업 영역의 공유 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43322-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="43322-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43322-114">PARAMETERS</span></span>

### <span data-ttu-id="43322-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43322-115">-DefaultProfile</span></span>
<span data-ttu-id="43322-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43322-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43322-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43322-117">-Name</span></span>
<span data-ttu-id="43322-118">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43322-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="43322-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43322-119">-ResourceGroupName</span></span>
<span data-ttu-id="43322-120">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43322-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="43322-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43322-121">CommonParameters</span></span>
<span data-ttu-id="43322-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43322-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43322-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="43322-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43322-124">입력</span><span class="sxs-lookup"><span data-stu-id="43322-124">INPUTS</span></span>

### <span data-ttu-id="43322-125">System.String</span><span class="sxs-lookup"><span data-stu-id="43322-125">System.String</span></span>

## <span data-ttu-id="43322-126">출력</span><span class="sxs-lookup"><span data-stu-id="43322-126">OUTPUTS</span></span>

### <span data-ttu-id="43322-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="43322-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="43322-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43322-128">NOTES</span></span>

## <span data-ttu-id="43322-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43322-129">RELATED LINKS</span></span>

[<span data-ttu-id="43322-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43322-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="43322-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="43322-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


