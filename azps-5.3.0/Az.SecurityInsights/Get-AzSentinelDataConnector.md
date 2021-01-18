---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494944"
---
# <span data-ttu-id="8123a-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8123a-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="8123a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8123a-102">SYNOPSIS</span></span>
<span data-ttu-id="8123a-103">데이터 커넥터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-103">Get a Data Connector.</span></span>

## <span data-ttu-id="8123a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8123a-104">SYNTAX</span></span>

### <span data-ttu-id="8123a-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="8123a-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8123a-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="8123a-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8123a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8123a-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8123a-108">설명</span><span class="sxs-lookup"><span data-stu-id="8123a-108">DESCRIPTION</span></span>
<span data-ttu-id="8123a-109">**Get-AzSentinelDataConnector** cmdlet은 지정된 작업 영역의 데이터 커넥터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="8123a-110">*DataConnectorId* 매개 변수를 지정하면 단일 **DataConnector 개체가** 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="8123a-111">*DataConnectorId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 데이터 커넥터를 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="8123a-112">**DataConnector** 개체를 사용하여 Data Connector를 업데이트할 수 있습니다. 예를 들어 **DataConnector를** 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="8123a-113">예제</span><span class="sxs-lookup"><span data-stu-id="8123a-113">EXAMPLES</span></span>

### <span data-ttu-id="8123a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="8123a-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="8123a-115">이 예제에서는 지정된 작업 영역의 **모든 DataConnectors를** 한 다음, $DataConnectors 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="8123a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="8123a-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="8123a-117">이 예제에서는 지정된 작업 영역의 **DataConnector를** 한 다음, 데이터 $DataConnector 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="8123a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8123a-118">PARAMETERS</span></span>

### <span data-ttu-id="8123a-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="8123a-119">-DataConnectorId</span></span>
<span data-ttu-id="8123a-120">데이터 커넥터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="8123a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8123a-121">-DefaultProfile</span></span>
<span data-ttu-id="8123a-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8123a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8123a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8123a-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-124">Resource group name.</span></span>

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

### <span data-ttu-id="8123a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8123a-125">-ResourceId</span></span>
<span data-ttu-id="8123a-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-126">Resource Id.</span></span>

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

### <span data-ttu-id="8123a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8123a-127">-WorkspaceName</span></span>
<span data-ttu-id="8123a-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-128">Workspace Name.</span></span>

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

### <span data-ttu-id="8123a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8123a-129">CommonParameters</span></span>
<span data-ttu-id="8123a-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8123a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8123a-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8123a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8123a-132">입력</span><span class="sxs-lookup"><span data-stu-id="8123a-132">INPUTS</span></span>

### <span data-ttu-id="8123a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8123a-133">System.String</span></span>
## <span data-ttu-id="8123a-134">출력</span><span class="sxs-lookup"><span data-stu-id="8123a-134">OUTPUTS</span></span>

### <span data-ttu-id="8123a-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="8123a-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="8123a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8123a-136">NOTES</span></span>

## <span data-ttu-id="8123a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8123a-137">RELATED LINKS</span></span>
