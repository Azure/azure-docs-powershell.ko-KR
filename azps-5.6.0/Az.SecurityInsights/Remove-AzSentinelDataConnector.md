---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978128"
---
# <span data-ttu-id="62e5b-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="62e5b-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="62e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="62e5b-103">데이터 커넥터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="62e5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="62e5b-104">SYNTAX</span></span>

### <span data-ttu-id="62e5b-105">DataConnectorId(기본값)</span><span class="sxs-lookup"><span data-stu-id="62e5b-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e5b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="62e5b-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e5b-107">설명</span><span class="sxs-lookup"><span data-stu-id="62e5b-107">DESCRIPTION</span></span>
<span data-ttu-id="62e5b-108">**Remove-AzSentinelDataConnector** cmdlet은 지정된 작업 영역의 데이터 커넥터를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="62e5b-109">파이프라인 연산자를 사용하여 **DataConnector** 개체를 전달하거나 또는 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="62e5b-110">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="62e5b-111">예제</span><span class="sxs-lookup"><span data-stu-id="62e5b-111">EXAMPLES</span></span>

### <span data-ttu-id="62e5b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="62e5b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="62e5b-113">이 명령은 작업 영역에서 DataConnector를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="62e5b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="62e5b-114">PARAMETERS</span></span>

### <span data-ttu-id="62e5b-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="62e5b-115">-DataConnectorId</span></span>
<span data-ttu-id="62e5b-116">데이터 커넥터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e5b-117">-DefaultProfile</span></span>
<span data-ttu-id="62e5b-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62e5b-119">-InputObject</span></span>
<span data-ttu-id="62e5b-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="62e5b-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62e5b-121">-PassThru</span></span>
<span data-ttu-id="62e5b-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="62e5b-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="62e5b-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62e5b-125">-WorkspaceName</span></span>
<span data-ttu-id="62e5b-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="62e5b-127">-Confirm</span></span>
<span data-ttu-id="62e5b-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e5b-129">-WhatIf</span></span>
<span data-ttu-id="62e5b-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e5b-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e5b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e5b-132">CommonParameters</span></span>
<span data-ttu-id="62e5b-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62e5b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e5b-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62e5b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e5b-135">입력</span><span class="sxs-lookup"><span data-stu-id="62e5b-135">INPUTS</span></span>

### <span data-ttu-id="62e5b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="62e5b-136">System.String</span></span>
### <span data-ttu-id="62e5b-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="62e5b-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="62e5b-138">출력</span><span class="sxs-lookup"><span data-stu-id="62e5b-138">OUTPUTS</span></span>

### <span data-ttu-id="62e5b-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="62e5b-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="62e5b-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62e5b-140">NOTES</span></span>

## <span data-ttu-id="62e5b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62e5b-141">RELATED LINKS</span></span>
