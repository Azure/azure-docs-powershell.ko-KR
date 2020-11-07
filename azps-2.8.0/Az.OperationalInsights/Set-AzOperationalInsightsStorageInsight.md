---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b81d7e7d87e8db7658db425f889630a3897d1ecd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880166"
---
# <span data-ttu-id="c8773-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c8773-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="c8773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8773-102">SYNOPSIS</span></span>
<span data-ttu-id="c8773-103">저장소 통찰력을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="c8773-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8773-104">SYNTAX</span></span>

### <span data-ttu-id="c8773-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c8773-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8773-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8773-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8773-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c8773-107">DESCRIPTION</span></span>
<span data-ttu-id="c8773-108">**AzOperationalInsightsStorageInsight** Cmdlet은 저장소 파악의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="c8773-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c8773-109">EXAMPLES</span></span>

### <span data-ttu-id="c8773-110">예제 1: 이름으로 저장소를 파악 하 여 수정</span><span class="sxs-lookup"><span data-stu-id="c8773-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c8773-111">이 명령은 저장소에 대 한 MyStorageInsight이 지정 된 테이블을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="c8773-112">예제 2: workspace 개체를 사용 하 여 저장소 통찰력 수정</span><span class="sxs-lookup"><span data-stu-id="c8773-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="c8773-113">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="c8773-114">두 번째 명령은 저장소에 대 한 MyStorageInsight이 지정 된 컨테이너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="c8773-115">변수</span><span class="sxs-lookup"><span data-stu-id="c8773-115">PARAMETERS</span></span>

### <span data-ttu-id="c8773-116">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="c8773-116">-Containers</span></span>
<span data-ttu-id="c8773-117">데이터를 제공 하는 컨테이너의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8773-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8773-118">-DefaultProfile</span></span>
<span data-ttu-id="c8773-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c8773-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8773-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c8773-120">-Name</span></span>
<span data-ttu-id="c8773-121">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8773-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8773-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8773-123">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c8773-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c8773-124">-StorageAccountKey</span></span>
<span data-ttu-id="c8773-125">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8773-126">-테이블</span><span class="sxs-lookup"><span data-stu-id="c8773-126">-Tables</span></span>
<span data-ttu-id="c8773-127">데이터를 포함 하는 테이블의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8773-128">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="c8773-128">-Workspace</span></span>
<span data-ttu-id="c8773-129">저장소 정보가 포함 된 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="c8773-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8773-130">-WorkspaceName</span></span>
<span data-ttu-id="c8773-131">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="c8773-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8773-132">CommonParameters</span></span>
<span data-ttu-id="c8773-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8773-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8773-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8773-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8773-135">입력</span><span class="sxs-lookup"><span data-stu-id="c8773-135">INPUTS</span></span>

### <span data-ttu-id="c8773-136">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="c8773-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c8773-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c8773-137">System.String</span></span>

### <span data-ttu-id="c8773-138">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="c8773-138">System.String[]</span></span>

## <span data-ttu-id="c8773-139">출력</span><span class="sxs-lookup"><span data-stu-id="c8773-139">OUTPUTS</span></span>

### <span data-ttu-id="c8773-140">OperationalInsights. PSStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="c8773-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="c8773-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c8773-141">NOTES</span></span>

## <span data-ttu-id="c8773-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8773-142">RELATED LINKS</span></span>

[<span data-ttu-id="c8773-143">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8773-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c8773-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8773-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


