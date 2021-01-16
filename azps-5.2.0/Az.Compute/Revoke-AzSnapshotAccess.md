---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336009"
---
# <span data-ttu-id="163a8-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="163a8-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="163a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="163a8-102">SYNOPSIS</span></span>
<span data-ttu-id="163a8-103">스냅숏에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="163a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="163a8-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="163a8-105">설명</span><span class="sxs-lookup"><span data-stu-id="163a8-105">DESCRIPTION</span></span>
<span data-ttu-id="163a8-106">**Revoke-AzSnapshotAccess** cmdlet은 스냅숏에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="163a8-107">예제</span><span class="sxs-lookup"><span data-stu-id="163a8-107">EXAMPLES</span></span>

### <span data-ttu-id="163a8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="163a8-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="163a8-109">'ResourceGroup01'이라는 리소스 그룹에서 'Snapshot01'이라는 스냅숏에 대한 액세스를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="163a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="163a8-110">PARAMETERS</span></span>

### <span data-ttu-id="163a8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="163a8-111">-AsJob</span></span>
<span data-ttu-id="163a8-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="163a8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="163a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163a8-113">-DefaultProfile</span></span>
<span data-ttu-id="163a8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="163a8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163a8-115">-ResourceGroupName</span></span>
<span data-ttu-id="163a8-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="163a8-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="163a8-117">-SnapshotName</span></span>
<span data-ttu-id="163a8-118">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="163a8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="163a8-119">-Confirm</span></span>
<span data-ttu-id="163a8-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="163a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="163a8-121">-WhatIf</span></span>
<span data-ttu-id="163a8-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="163a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="163a8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="163a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163a8-124">CommonParameters</span></span>
<span data-ttu-id="163a8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="163a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163a8-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="163a8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163a8-127">입력</span><span class="sxs-lookup"><span data-stu-id="163a8-127">INPUTS</span></span>

### <span data-ttu-id="163a8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="163a8-128">System.String</span></span>

## <span data-ttu-id="163a8-129">출력</span><span class="sxs-lookup"><span data-stu-id="163a8-129">OUTPUTS</span></span>

### <span data-ttu-id="163a8-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="163a8-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="163a8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="163a8-131">NOTES</span></span>

## <span data-ttu-id="163a8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="163a8-132">RELATED LINKS</span></span>
