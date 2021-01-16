---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366073"
---
# <span data-ttu-id="e054f-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="e054f-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="e054f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e054f-102">SYNOPSIS</span></span>
<span data-ttu-id="e054f-103">스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-103">Removes a snapshot.</span></span>

## <span data-ttu-id="e054f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e054f-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e054f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e054f-105">DESCRIPTION</span></span>
<span data-ttu-id="e054f-106">**Remove-AzSnapshot** cmdlet은 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="e054f-107">예제</span><span class="sxs-lookup"><span data-stu-id="e054f-107">EXAMPLES</span></span>

### <span data-ttu-id="e054f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e054f-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="e054f-109">이 명령은 리소스 그룹 'ResourceGroup01'에서 'Snapshot01'이라는 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e054f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e054f-110">PARAMETERS</span></span>

### <span data-ttu-id="e054f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e054f-111">-AsJob</span></span>
<span data-ttu-id="e054f-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e054f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e054f-113">-DefaultProfile</span></span>
<span data-ttu-id="e054f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e054f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e054f-115">-Force</span></span>
<span data-ttu-id="e054f-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e054f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e054f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e054f-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e054f-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e054f-119">-SnapshotName</span></span>
<span data-ttu-id="e054f-120">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e054f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e054f-121">-Confirm</span></span>
<span data-ttu-id="e054f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e054f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e054f-123">-WhatIf</span></span>
<span data-ttu-id="e054f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e054f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e054f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e054f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e054f-126">CommonParameters</span></span>
<span data-ttu-id="e054f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e054f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e054f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e054f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e054f-129">입력</span><span class="sxs-lookup"><span data-stu-id="e054f-129">INPUTS</span></span>

### <span data-ttu-id="e054f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e054f-130">System.String</span></span>

## <span data-ttu-id="e054f-131">출력</span><span class="sxs-lookup"><span data-stu-id="e054f-131">OUTPUTS</span></span>

### <span data-ttu-id="e054f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e054f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e054f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e054f-133">NOTES</span></span>

## <span data-ttu-id="e054f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e054f-134">RELATED LINKS</span></span>
