---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041567"
---
# <span data-ttu-id="9ae5b-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9ae5b-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="9ae5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae5b-103">스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="9ae5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ae5b-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ae5b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ae5b-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae5b-106">**AzSnapshotAccess** cmdlet은 스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="9ae5b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ae5b-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae5b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ae5b-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="9ae5b-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '에 ' Snapshot01 ' 이라는 스냅숏에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="9ae5b-110">변수</span><span class="sxs-lookup"><span data-stu-id="9ae5b-110">PARAMETERS</span></span>

### <span data-ttu-id="9ae5b-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9ae5b-111">-Access</span></span>
<span data-ttu-id="9ae5b-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="9ae5b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ae5b-113">-AsJob</span></span>
<span data-ttu-id="9ae5b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ae5b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ae5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae5b-115">-DefaultProfile</span></span>
<span data-ttu-id="9ae5b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ae5b-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="9ae5b-117">-DurationInSecond</span></span>
<span data-ttu-id="9ae5b-118">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="9ae5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ae5b-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ae5b-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9ae5b-121">-SnapshotName</span></span>
<span data-ttu-id="9ae5b-122">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9ae5b-123">-확인</span><span class="sxs-lookup"><span data-stu-id="9ae5b-123">-Confirm</span></span>
<span data-ttu-id="9ae5b-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae5b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae5b-125">-WhatIf</span></span>
<span data-ttu-id="9ae5b-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ae5b-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae5b-128">CommonParameters</span></span>
<span data-ttu-id="9ae5b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae5b-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ae5b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae5b-131">입력</span><span class="sxs-lookup"><span data-stu-id="9ae5b-131">INPUTS</span></span>

### <span data-ttu-id="9ae5b-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ae5b-132">System.String</span></span>

## <span data-ttu-id="9ae5b-133">출력</span><span class="sxs-lookup"><span data-stu-id="9ae5b-133">OUTPUTS</span></span>

### <span data-ttu-id="9ae5b-134">Microsoft. i. m a. 모델. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="9ae5b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="9ae5b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="9ae5b-135">NOTES</span></span>

## <span data-ttu-id="9ae5b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ae5b-136">RELATED LINKS</span></span>
