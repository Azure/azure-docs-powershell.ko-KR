---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 589b6012a1819eac638f6197d0569972e4727fba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880001"
---
# <span data-ttu-id="21c14-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="21c14-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="21c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c14-102">SYNOPSIS</span></span>
<span data-ttu-id="21c14-103">저장소 통찰에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="21c14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21c14-104">SYNTAX</span></span>

### <span data-ttu-id="21c14-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="21c14-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c14-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="21c14-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c14-107">설명은</span><span class="sxs-lookup"><span data-stu-id="21c14-107">DESCRIPTION</span></span>
<span data-ttu-id="21c14-108">**AzOperationalInsightsStorageInsight** cmdlet은 기존 저장소 통찰에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="21c14-109">저장소 정보를 지정 하는 경우이 cmdlet은 해당 저장소를 파악 하는 데 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="21c14-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 storage insights에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="21c14-111">예제의</span><span class="sxs-lookup"><span data-stu-id="21c14-111">EXAMPLES</span></span>

### <span data-ttu-id="21c14-112">예제 1: 이름으로 저장소를 파악 하세요.</span><span class="sxs-lookup"><span data-stu-id="21c14-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="21c14-113">이 명령은 ContosoWorkspace 이라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="21c14-114">예제 2: workspace 개체를 사용 하 여 저장소를 파악 하세요.</span><span class="sxs-lookup"><span data-stu-id="21c14-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="21c14-115">첫 번째 명령은 **AzOperationalInsightsWorkspace** cmdlet을 사용 하 여 Operational Insights 작업 영역을 얻은 다음 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="21c14-116">두 번째 명령은 $Workspace의 작업 영역에 대 한 MyStorageInsight 이라는 저장소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="21c14-117">변수</span><span class="sxs-lookup"><span data-stu-id="21c14-117">PARAMETERS</span></span>

### <span data-ttu-id="21c14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c14-118">-DefaultProfile</span></span>
<span data-ttu-id="21c14-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="21c14-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c14-120">-이름</span><span class="sxs-lookup"><span data-stu-id="21c14-120">-Name</span></span>
<span data-ttu-id="21c14-121">저장소 통찰 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c14-122">-ResourceGroupName</span></span>
<span data-ttu-id="21c14-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c14-124">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="21c14-124">-Workspace</span></span>
<span data-ttu-id="21c14-125">저장소 정보 활용이 포함 된 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c14-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21c14-126">-WorkspaceName</span></span>
<span data-ttu-id="21c14-127">저장소 정보 활용이 포함 된 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c14-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c14-128">CommonParameters</span></span>
<span data-ttu-id="21c14-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c14-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c14-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c14-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c14-131">입력</span><span class="sxs-lookup"><span data-stu-id="21c14-131">INPUTS</span></span>

### <span data-ttu-id="21c14-132">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="21c14-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="21c14-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="21c14-133">System.String</span></span>

## <span data-ttu-id="21c14-134">출력</span><span class="sxs-lookup"><span data-stu-id="21c14-134">OUTPUTS</span></span>

### <span data-ttu-id="21c14-135">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="21c14-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="21c14-136">상속자</span><span class="sxs-lookup"><span data-stu-id="21c14-136">NOTES</span></span>

## <span data-ttu-id="21c14-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21c14-137">RELATED LINKS</span></span>

[<span data-ttu-id="21c14-138">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21c14-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


