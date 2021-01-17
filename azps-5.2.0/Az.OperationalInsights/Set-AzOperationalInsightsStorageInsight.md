---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346173"
---
# <span data-ttu-id="9d50c-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="9d50c-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="9d50c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d50c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d50c-103">Storage 인사이트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="9d50c-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d50c-104">SYNTAX</span></span>

### <span data-ttu-id="9d50c-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9d50c-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d50c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9d50c-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d50c-107">설명</span><span class="sxs-lookup"><span data-stu-id="9d50c-107">DESCRIPTION</span></span>
<span data-ttu-id="9d50c-108">**Set-AzOperationalInsightsStorageInsight** cmdlet은 Storage Insight의 구성을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="9d50c-109">예제</span><span class="sxs-lookup"><span data-stu-id="9d50c-109">EXAMPLES</span></span>

### <span data-ttu-id="9d50c-110">예제 1: 이름으로 Storage 인사이트 수정</span><span class="sxs-lookup"><span data-stu-id="9d50c-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="9d50c-111">이 명령은 MyStorageInsight라는 Storage Insight가 읽는 테이블을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="9d50c-112">예제 2: 작업 영역 개체를 사용하여 Storage 인사이트 수정</span><span class="sxs-lookup"><span data-stu-id="9d50c-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="9d50c-113">첫 번째 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음, $Workspace 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="9d50c-114">두 번째 명령은 MyStorageInsight라는 Storage Insight가 읽는 컨테이너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="9d50c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d50c-115">PARAMETERS</span></span>

### <span data-ttu-id="9d50c-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="9d50c-116">-Containers</span></span>
<span data-ttu-id="9d50c-117">데이터를 제공하는 컨테이너 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="9d50c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d50c-118">-DefaultProfile</span></span>
<span data-ttu-id="9d50c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d50c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d50c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9d50c-120">-Name</span></span>
<span data-ttu-id="9d50c-121">Storage 인사이트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="9d50c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d50c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d50c-123">작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="9d50c-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9d50c-124">-StorageAccountKey</span></span>
<span data-ttu-id="9d50c-125">저장소 계정에 대한 액세스 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="9d50c-126">-Tables</span><span class="sxs-lookup"><span data-stu-id="9d50c-126">-Tables</span></span>
<span data-ttu-id="9d50c-127">데이터가 포함된 테이블 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="9d50c-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9d50c-128">-Workspace</span></span>
<span data-ttu-id="9d50c-129">Storage 인사이트를 포함하는 작업 공간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="9d50c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d50c-130">-WorkspaceName</span></span>
<span data-ttu-id="9d50c-131">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="9d50c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d50c-132">CommonParameters</span></span>
<span data-ttu-id="9d50c-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d50c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d50c-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9d50c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d50c-135">입력</span><span class="sxs-lookup"><span data-stu-id="9d50c-135">INPUTS</span></span>

### <span data-ttu-id="9d50c-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d50c-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9d50c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9d50c-137">System.String</span></span>

### <span data-ttu-id="9d50c-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9d50c-138">System.String[]</span></span>

## <span data-ttu-id="9d50c-139">출력</span><span class="sxs-lookup"><span data-stu-id="9d50c-139">OUTPUTS</span></span>

### <span data-ttu-id="9d50c-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="9d50c-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="9d50c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d50c-141">NOTES</span></span>

## <span data-ttu-id="9d50c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d50c-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d50c-143">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9d50c-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="9d50c-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d50c-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


