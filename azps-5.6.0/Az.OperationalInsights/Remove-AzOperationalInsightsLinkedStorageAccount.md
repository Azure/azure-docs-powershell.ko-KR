---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989786"
---
# <span data-ttu-id="316c9-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="316c9-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="316c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316c9-102">SYNOPSIS</span></span>
<span data-ttu-id="316c9-103">작업 영역의 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="316c9-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="316c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="316c9-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="316c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="316c9-105">DESCRIPTION</span></span>
<span data-ttu-id="316c9-106">작업 영역의 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="316c9-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="316c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="316c9-107">EXAMPLES</span></span>

### <span data-ttu-id="316c9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="316c9-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="316c9-109">{workspace-name}에 대해 "CustomLogs"를 입력하여 연결된 저장소 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="316c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="316c9-110">PARAMETERS</span></span>

### <span data-ttu-id="316c9-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="316c9-111">-DataSourceType</span></span>
<span data-ttu-id="316c9-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316c9-113">-DefaultProfile</span></span>
<span data-ttu-id="316c9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="316c9-115">-Force</span></span>
<span data-ttu-id="316c9-116">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="316c9-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="316c9-119">-WorkspaceName</span></span>
<span data-ttu-id="316c9-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-120">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-121">-확인</span><span class="sxs-lookup"><span data-stu-id="316c9-121">-Confirm</span></span>
<span data-ttu-id="316c9-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316c9-123">-WhatIf</span></span>
<span data-ttu-id="316c9-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316c9-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316c9-126">CommonParameters</span></span>
<span data-ttu-id="316c9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="316c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316c9-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="316c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316c9-129">입력</span><span class="sxs-lookup"><span data-stu-id="316c9-129">INPUTS</span></span>

### <span data-ttu-id="316c9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="316c9-130">System.String</span></span>

## <span data-ttu-id="316c9-131">출력</span><span class="sxs-lookup"><span data-stu-id="316c9-131">OUTPUTS</span></span>

### <span data-ttu-id="316c9-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="316c9-132">System.Boolean</span></span>

## <span data-ttu-id="316c9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="316c9-133">NOTES</span></span>

## <span data-ttu-id="316c9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="316c9-134">RELATED LINKS</span></span>
