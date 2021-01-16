---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342026"
---
# <span data-ttu-id="f915c-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f915c-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f915c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f915c-102">SYNOPSIS</span></span>
<span data-ttu-id="f915c-103">작업 영역의 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="f915c-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="f915c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f915c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f915c-105">설명</span><span class="sxs-lookup"><span data-stu-id="f915c-105">DESCRIPTION</span></span>
<span data-ttu-id="f915c-106">작업 영역의 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="f915c-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="f915c-107">예제</span><span class="sxs-lookup"><span data-stu-id="f915c-107">EXAMPLES</span></span>

### <span data-ttu-id="f915c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f915c-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="f915c-109">{workspace-name}에 대해 "CustomLogs" 형식의 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="f915c-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="f915c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f915c-110">PARAMETERS</span></span>

### <span data-ttu-id="f915c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="f915c-111">-DataSourceType</span></span>
<span data-ttu-id="f915c-112">데이터 원본 형식은 'CustomLogs', 'AzureWatson' 중 하나해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="f915c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f915c-113">-DefaultProfile</span></span>
<span data-ttu-id="f915c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f915c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f915c-115">-Force</span></span>
<span data-ttu-id="f915c-116">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f915c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f915c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f915c-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-118">The resource group name.</span></span>

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

### <span data-ttu-id="f915c-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f915c-119">-WorkspaceName</span></span>
<span data-ttu-id="f915c-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-120">The workspace name.</span></span>

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

### <span data-ttu-id="f915c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f915c-121">-Confirm</span></span>
<span data-ttu-id="f915c-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f915c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f915c-123">-WhatIf</span></span>
<span data-ttu-id="f915c-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f915c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f915c-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f915c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f915c-126">CommonParameters</span></span>
<span data-ttu-id="f915c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f915c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f915c-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f915c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f915c-129">입력</span><span class="sxs-lookup"><span data-stu-id="f915c-129">INPUTS</span></span>

### <span data-ttu-id="f915c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f915c-130">System.String</span></span>

## <span data-ttu-id="f915c-131">출력</span><span class="sxs-lookup"><span data-stu-id="f915c-131">OUTPUTS</span></span>

### <span data-ttu-id="f915c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f915c-132">System.Boolean</span></span>

## <span data-ttu-id="f915c-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f915c-133">NOTES</span></span>

## <span data-ttu-id="f915c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f915c-134">RELATED LINKS</span></span>
