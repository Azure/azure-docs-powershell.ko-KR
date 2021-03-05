---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 86eb9f1389f0474fcc109b219e9eae1bd385b7b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991475"
---
# <span data-ttu-id="73c1b-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="73c1b-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="73c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="73c1b-103">스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-103">Removes a snapshot.</span></span>

## <span data-ttu-id="73c1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="73c1b-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="73c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="73c1b-106">**Remove-AzSnapshot** cmdlet은 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="73c1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="73c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="73c1b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="73c1b-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="73c1b-109">이 명령은 리소스 그룹 'ResourceGroup01'에서 '스냅숏01'이라는 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="73c1b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="73c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="73c1b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73c1b-111">-AsJob</span></span>
<span data-ttu-id="73c1b-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="73c1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c1b-113">-DefaultProfile</span></span>
<span data-ttu-id="73c1b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c1b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="73c1b-115">-Force</span></span>
<span data-ttu-id="73c1b-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73c1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="73c1b-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73c1b-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="73c1b-119">-SnapshotName</span></span>
<span data-ttu-id="73c1b-120">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="73c1b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="73c1b-121">-Confirm</span></span>
<span data-ttu-id="73c1b-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c1b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c1b-123">-WhatIf</span></span>
<span data-ttu-id="73c1b-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c1b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c1b-126">CommonParameters</span></span>
<span data-ttu-id="73c1b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73c1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c1b-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73c1b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c1b-129">입력</span><span class="sxs-lookup"><span data-stu-id="73c1b-129">INPUTS</span></span>

### <span data-ttu-id="73c1b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73c1b-130">System.String</span></span>

## <span data-ttu-id="73c1b-131">출력</span><span class="sxs-lookup"><span data-stu-id="73c1b-131">OUTPUTS</span></span>

### <span data-ttu-id="73c1b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="73c1b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="73c1b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73c1b-133">NOTES</span></span>

## <span data-ttu-id="73c1b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73c1b-134">RELATED LINKS</span></span>
