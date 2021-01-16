---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334317"
---
# <span data-ttu-id="dd548-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="dd548-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="dd548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd548-102">SYNOPSIS</span></span>
<span data-ttu-id="dd548-103">스냅숏에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="dd548-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd548-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd548-105">설명</span><span class="sxs-lookup"><span data-stu-id="dd548-105">DESCRIPTION</span></span>
<span data-ttu-id="dd548-106">**Grant-AzSnapshotAccess** cmdlet은 스냅숏에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="dd548-107">예제</span><span class="sxs-lookup"><span data-stu-id="dd548-107">EXAMPLES</span></span>

### <span data-ttu-id="dd548-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd548-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="dd548-109">60초 동안 'ResourceGroup01'이라는 리소스 그룹의 'Snapshot01'이라는 스냅숏에 '읽기' 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="dd548-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd548-110">PARAMETERS</span></span>

### <span data-ttu-id="dd548-111">-Access</span><span class="sxs-lookup"><span data-stu-id="dd548-111">-Access</span></span>
<span data-ttu-id="dd548-112">액세스 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd548-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd548-113">-AsJob</span></span>
<span data-ttu-id="dd548-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dd548-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd548-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd548-115">-DefaultProfile</span></span>
<span data-ttu-id="dd548-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd548-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="dd548-117">-DurationInSecond</span></span>
<span data-ttu-id="dd548-118">액세스 기간을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd548-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd548-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd548-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dd548-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="dd548-121">-SnapshotName</span></span>
<span data-ttu-id="dd548-122">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="dd548-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd548-123">-Confirm</span></span>
<span data-ttu-id="dd548-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd548-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd548-125">-WhatIf</span></span>
<span data-ttu-id="dd548-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dd548-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd548-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd548-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd548-128">CommonParameters</span></span>
<span data-ttu-id="dd548-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd548-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd548-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd548-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd548-131">입력</span><span class="sxs-lookup"><span data-stu-id="dd548-131">INPUTS</span></span>

### <span data-ttu-id="dd548-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dd548-132">System.String</span></span>

## <span data-ttu-id="dd548-133">출력</span><span class="sxs-lookup"><span data-stu-id="dd548-133">OUTPUTS</span></span>

### <span data-ttu-id="dd548-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="dd548-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="dd548-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd548-135">NOTES</span></span>

## <span data-ttu-id="dd548-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd548-136">RELATED LINKS</span></span>
