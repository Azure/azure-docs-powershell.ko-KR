---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881998"
---
# <span data-ttu-id="22e30-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="22e30-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="22e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e30-102">SYNOPSIS</span></span>
<span data-ttu-id="22e30-103">스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22e30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22e30-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22e30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22e30-105">DESCRIPTION</span></span>
<span data-ttu-id="22e30-106">**AzureRmSnapshotAccess** cmdlet은 스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="22e30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22e30-107">EXAMPLES</span></span>

### <span data-ttu-id="22e30-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="22e30-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="22e30-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '에 ' Snapshot01 ' 이라는 스냅숏에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="22e30-110">변수</span><span class="sxs-lookup"><span data-stu-id="22e30-110">PARAMETERS</span></span>

### <span data-ttu-id="22e30-111">-Access</span><span class="sxs-lookup"><span data-stu-id="22e30-111">-Access</span></span>
<span data-ttu-id="22e30-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22e30-113">-AsJob</span></span>
<span data-ttu-id="22e30-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22e30-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22e30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e30-115">-DefaultProfile</span></span>
<span data-ttu-id="22e30-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e30-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="22e30-117">-DurationInSecond</span></span>
<span data-ttu-id="22e30-118">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-118">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e30-119">-ResourceGroupName</span></span>
<span data-ttu-id="22e30-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e30-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="22e30-121">-SnapshotName</span></span>
<span data-ttu-id="22e30-122">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e30-123">-확인</span><span class="sxs-lookup"><span data-stu-id="22e30-123">-Confirm</span></span>
<span data-ttu-id="22e30-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e30-125">-WhatIf</span></span>
<span data-ttu-id="22e30-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22e30-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e30-128">CommonParameters</span></span>
<span data-ttu-id="22e30-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e30-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e30-131">입력</span><span class="sxs-lookup"><span data-stu-id="22e30-131">INPUTS</span></span>

### <span data-ttu-id="22e30-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22e30-132">System.String</span></span>

## <span data-ttu-id="22e30-133">출력</span><span class="sxs-lookup"><span data-stu-id="22e30-133">OUTPUTS</span></span>

### <span data-ttu-id="22e30-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="22e30-134">System.Object</span></span>

## <span data-ttu-id="22e30-135">상속자</span><span class="sxs-lookup"><span data-stu-id="22e30-135">NOTES</span></span>

## <span data-ttu-id="22e30-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22e30-136">RELATED LINKS</span></span>

