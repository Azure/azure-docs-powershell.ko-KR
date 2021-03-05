---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: b99ad26ddfa0239f073c4179413b2f1fefec4d1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986449"
---
# <span data-ttu-id="ee093-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ee093-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="ee093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee093-102">SYNOPSIS</span></span>
<span data-ttu-id="ee093-103">데이터 커넥터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-103">Get a Data Connector.</span></span>

## <span data-ttu-id="ee093-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee093-104">SYNTAX</span></span>

### <span data-ttu-id="ee093-105">작업 영역Scope(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee093-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee093-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="ee093-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee093-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee093-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee093-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee093-108">DESCRIPTION</span></span>
<span data-ttu-id="ee093-109">**Get-AzSentinelDataConnector** cmdlet은 지정된 작업 영역에서 데이터 커넥터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="ee093-110">*DataConnectorId* 매개 변수를 지정하면 **단일 DataConnector 개체가** 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="ee093-111">*DataConnectorId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 데이터 커넥터를 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="ee093-112">**DataConnector** 개체를 사용하여 Data Connector를 업데이트할 수 있습니다(예: **DataConnector를** 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="ee093-113">예제</span><span class="sxs-lookup"><span data-stu-id="ee093-113">EXAMPLES</span></span>

### <span data-ttu-id="ee093-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee093-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="ee093-115">이 예제에서는 지정된 작업 영역의 **모든 DataConnectors를** 한 다음, 데이터 $DataConnectors 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="ee093-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee093-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="ee093-117">이 예제에서는 지정된 작업 영역의 **DataConnector를** 한 다음, 데이터 $DataConnector 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="ee093-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ee093-118">PARAMETERS</span></span>

### <span data-ttu-id="ee093-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="ee093-119">-DataConnectorId</span></span>
<span data-ttu-id="ee093-120">데이터 커넥터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee093-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee093-121">-DefaultProfile</span></span>
<span data-ttu-id="ee093-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee093-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee093-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee093-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee093-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee093-125">-ResourceId</span></span>
<span data-ttu-id="ee093-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee093-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee093-127">-WorkspaceName</span></span>
<span data-ttu-id="ee093-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee093-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee093-129">CommonParameters</span></span>
<span data-ttu-id="ee093-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee093-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee093-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee093-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee093-132">입력</span><span class="sxs-lookup"><span data-stu-id="ee093-132">INPUTS</span></span>

### <span data-ttu-id="ee093-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee093-133">System.String</span></span>
## <span data-ttu-id="ee093-134">출력</span><span class="sxs-lookup"><span data-stu-id="ee093-134">OUTPUTS</span></span>

### <span data-ttu-id="ee093-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ee093-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="ee093-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee093-136">NOTES</span></span>

## <span data-ttu-id="ee093-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee093-137">RELATED LINKS</span></span>
