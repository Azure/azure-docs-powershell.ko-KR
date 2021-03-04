---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952795"
---
# <span data-ttu-id="b024d-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b024d-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="b024d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b024d-102">SYNOPSIS</span></span>
<span data-ttu-id="b024d-103">스냅숏에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="b024d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b024d-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b024d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b024d-105">DESCRIPTION</span></span>
<span data-ttu-id="b024d-106">**Revoke-AzSnapshotAccess** cmdlet은 스냅숏에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="b024d-107">예제</span><span class="sxs-lookup"><span data-stu-id="b024d-107">EXAMPLES</span></span>

### <span data-ttu-id="b024d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b024d-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="b024d-109">'ResourceGroup01'이라는 리소스 그룹에서 '스냅숏01'이라는 스냅숏에 대한 액세스 해지</span><span class="sxs-lookup"><span data-stu-id="b024d-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="b024d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b024d-110">PARAMETERS</span></span>

### <span data-ttu-id="b024d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b024d-111">-AsJob</span></span>
<span data-ttu-id="b024d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b024d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b024d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b024d-113">-DefaultProfile</span></span>
<span data-ttu-id="b024d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b024d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b024d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b024d-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b024d-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b024d-117">-SnapshotName</span></span>
<span data-ttu-id="b024d-118">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b024d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b024d-119">-Confirm</span></span>
<span data-ttu-id="b024d-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b024d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b024d-121">-WhatIf</span></span>
<span data-ttu-id="b024d-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b024d-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b024d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b024d-124">CommonParameters</span></span>
<span data-ttu-id="b024d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b024d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b024d-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b024d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b024d-127">입력</span><span class="sxs-lookup"><span data-stu-id="b024d-127">INPUTS</span></span>

### <span data-ttu-id="b024d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b024d-128">System.String</span></span>

## <span data-ttu-id="b024d-129">출력</span><span class="sxs-lookup"><span data-stu-id="b024d-129">OUTPUTS</span></span>

### <span data-ttu-id="b024d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b024d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b024d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b024d-131">NOTES</span></span>

## <span data-ttu-id="b024d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b024d-132">RELATED LINKS</span></span>
