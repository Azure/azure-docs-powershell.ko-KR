---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530146"
---
# <span data-ttu-id="0aa00-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0aa00-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="0aa00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aa00-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa00-103">저장소 통찰력을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aa00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0aa00-104">SYNTAX</span></span>

### <span data-ttu-id="0aa00-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0aa00-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa00-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0aa00-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa00-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0aa00-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa00-108">**AzureRmOperationalInsightsStorageInsight** cmdlet은 작업 영역에서 저장소 정보를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="0aa00-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0aa00-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa00-110">예제 1: 이름으로 저장 된 저장소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="0aa00-111">이 명령은 지정 된 리소스 그룹의 MyWorkspace 라는 작업 영역에서 MyStorageInsight 이라는 저장소 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="0aa00-112">명령에서 *Force* 매개 변수를 지정 하지 않으므로 저장소 정보를 제거 하기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="0aa00-113">예제 2: 확인 하지 않고 저장소 정보 제거</span><span class="sxs-lookup"><span data-stu-id="0aa00-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="0aa00-114">첫 번째 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고이를 $Workspace 변수에 저장 합니다. 두 번째 명령은 확인 메시지가 표시 되지 않고 $Workspace에서 MyStorageInsight 이라는 저장소 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="0aa00-115">변수</span><span class="sxs-lookup"><span data-stu-id="0aa00-115">PARAMETERS</span></span>

### <span data-ttu-id="0aa00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa00-116">-DefaultProfile</span></span>
<span data-ttu-id="0aa00-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0aa00-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa00-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0aa00-118">-Force</span></span>
<span data-ttu-id="0aa00-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0aa00-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0aa00-120">-Name</span></span>
<span data-ttu-id="0aa00-121">저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="0aa00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa00-122">-ResourceGroupName</span></span>
<span data-ttu-id="0aa00-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0aa00-124">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="0aa00-124">-Workspace</span></span>
<span data-ttu-id="0aa00-125">저장소 정보가 포함 된 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="0aa00-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0aa00-126">-WorkspaceName</span></span>
<span data-ttu-id="0aa00-127">저장소 정보를 포함 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="0aa00-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0aa00-128">-Confirm</span></span>
<span data-ttu-id="0aa00-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa00-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa00-130">-WhatIf</span></span>
<span data-ttu-id="0aa00-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa00-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa00-133">CommonParameters</span></span>
<span data-ttu-id="0aa00-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa00-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa00-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa00-136">입력</span><span class="sxs-lookup"><span data-stu-id="0aa00-136">INPUTS</span></span>

### <span data-ttu-id="0aa00-137">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="0aa00-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="0aa00-138">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0aa00-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="0aa00-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0aa00-139">System.String</span></span>

## <span data-ttu-id="0aa00-140">출력</span><span class="sxs-lookup"><span data-stu-id="0aa00-140">OUTPUTS</span></span>

### <span data-ttu-id="0aa00-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="0aa00-141">System.Void</span></span>

## <span data-ttu-id="0aa00-142">상속자</span><span class="sxs-lookup"><span data-stu-id="0aa00-142">NOTES</span></span>

## <span data-ttu-id="0aa00-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0aa00-143">RELATED LINKS</span></span>

[<span data-ttu-id="0aa00-144">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0aa00-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0aa00-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0aa00-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

