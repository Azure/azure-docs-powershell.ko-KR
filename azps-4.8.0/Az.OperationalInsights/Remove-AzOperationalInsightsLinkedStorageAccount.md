---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203838"
---
# <span data-ttu-id="28cee-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28cee-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="28cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cee-102">SYNOPSIS</span></span>
<span data-ttu-id="28cee-103">작업 영역에 대해 연결 된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="28cee-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="28cee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28cee-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28cee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28cee-105">DESCRIPTION</span></span>
<span data-ttu-id="28cee-106">작업 영역에 대해 연결 된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="28cee-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="28cee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28cee-107">EXAMPLES</span></span>

### <span data-ttu-id="28cee-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="28cee-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="28cee-109">"CustomLogs" 유형의 연결 된 저장소 계정 삭제 {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="28cee-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="28cee-110">변수</span><span class="sxs-lookup"><span data-stu-id="28cee-110">PARAMETERS</span></span>

### <span data-ttu-id="28cee-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="28cee-111">-DataSourceType</span></span>
<span data-ttu-id="28cee-112">데이터 원본 유형은 ' CustomLogs ', ' AzureWatson ' 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="28cee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cee-113">-DefaultProfile</span></span>
<span data-ttu-id="28cee-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28cee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28cee-115">-Force</span></span>
<span data-ttu-id="28cee-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="28cee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cee-117">-ResourceGroupName</span></span>
<span data-ttu-id="28cee-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-118">The resource group name.</span></span>

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

### <span data-ttu-id="28cee-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28cee-119">-WorkspaceName</span></span>
<span data-ttu-id="28cee-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-120">The workspace name.</span></span>

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

### <span data-ttu-id="28cee-121">-확인</span><span class="sxs-lookup"><span data-stu-id="28cee-121">-Confirm</span></span>
<span data-ttu-id="28cee-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cee-123">-WhatIf</span></span>
<span data-ttu-id="28cee-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cee-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cee-126">CommonParameters</span></span>
<span data-ttu-id="28cee-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cee-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28cee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cee-129">입력</span><span class="sxs-lookup"><span data-stu-id="28cee-129">INPUTS</span></span>

### <span data-ttu-id="28cee-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28cee-130">System.String</span></span>

## <span data-ttu-id="28cee-131">출력</span><span class="sxs-lookup"><span data-stu-id="28cee-131">OUTPUTS</span></span>

### <span data-ttu-id="28cee-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="28cee-132">System.Boolean</span></span>

## <span data-ttu-id="28cee-133">상속자</span><span class="sxs-lookup"><span data-stu-id="28cee-133">NOTES</span></span>

## <span data-ttu-id="28cee-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28cee-134">RELATED LINKS</span></span>
