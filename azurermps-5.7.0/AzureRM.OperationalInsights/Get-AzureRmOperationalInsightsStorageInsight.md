---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: e51325a18f8a880131e9037473a60e8a56ea488f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93711935"
---
# <span data-ttu-id="30df1-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="30df1-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="30df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30df1-102">SYNOPSIS</span></span>
<span data-ttu-id="30df1-103">저장소 통찰에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30df1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30df1-104">SYNTAX</span></span>

### <span data-ttu-id="30df1-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="30df1-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30df1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="30df1-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30df1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="30df1-107">DESCRIPTION</span></span>
<span data-ttu-id="30df1-108">**AzureRmOperationalInsightsStorageInsight** cmdlet은 기존 저장소 통찰에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="30df1-109">저장소 정보를 지정 하는 경우이 cmdlet은 해당 저장소를 파악 하는 데 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="30df1-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 storage insights에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="30df1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="30df1-111">EXAMPLES</span></span>

### <span data-ttu-id="30df1-112">예제 1: 이름으로 저장소를 파악 하세요.</span><span class="sxs-lookup"><span data-stu-id="30df1-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="30df1-113">이 명령은 ContosoWorkspace 이라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="30df1-114">예제 2: workspace 개체를 사용 하 여 저장소를 파악 하세요.</span><span class="sxs-lookup"><span data-stu-id="30df1-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="30df1-115">첫 번째 명령은 **AzureRmOperationalInsightsWorkspace** cmdlet을 사용 하 여 Operational Insights 작업 영역을 얻은 다음 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="30df1-116">두 번째 명령은 $Workspace의 작업 영역에 대 한 MyStorageInsight 이라는 저장소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="30df1-117">변수</span><span class="sxs-lookup"><span data-stu-id="30df1-117">PARAMETERS</span></span>

### <span data-ttu-id="30df1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30df1-118">-DefaultProfile</span></span>
<span data-ttu-id="30df1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30df1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30df1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="30df1-120">-Name</span></span>
<span data-ttu-id="30df1-121">저장소 통찰 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30df1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30df1-122">-ResourceGroupName</span></span>
<span data-ttu-id="30df1-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30df1-124">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="30df1-124">-Workspace</span></span>
<span data-ttu-id="30df1-125">저장소 정보 활용이 포함 된 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30df1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30df1-126">-WorkspaceName</span></span>
<span data-ttu-id="30df1-127">저장소 정보 활용이 포함 된 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30df1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30df1-128">CommonParameters</span></span>
<span data-ttu-id="30df1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30df1-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30df1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30df1-131">입력</span><span class="sxs-lookup"><span data-stu-id="30df1-131">INPUTS</span></span>

### <span data-ttu-id="30df1-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="30df1-132">PSWorkspace</span></span>
<span data-ttu-id="30df1-133">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="30df1-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="30df1-134">출력</span><span class="sxs-lookup"><span data-stu-id="30df1-134">OUTPUTS</span></span>

### <span data-ttu-id="30df1-135">System.webserver. List ' 1 [OperationalInsights. 모델. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="30df1-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="30df1-136">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="30df1-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="30df1-137">상속자</span><span class="sxs-lookup"><span data-stu-id="30df1-137">NOTES</span></span>

## <span data-ttu-id="30df1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30df1-138">RELATED LINKS</span></span>

[<span data-ttu-id="30df1-139">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30df1-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


