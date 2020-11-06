---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525324"
---
# <span data-ttu-id="35aaa-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="35aaa-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="35aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="35aaa-103">스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35aaa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35aaa-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35aaa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="35aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="35aaa-106">**AzureRmSnapshotAccess** cmdlet은 스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="35aaa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="35aaa-107">EXAMPLES</span></span>

### <span data-ttu-id="35aaa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="35aaa-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="35aaa-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '에 ' Snapshot01 ' 이라는 스냅숏에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="35aaa-110">변수</span><span class="sxs-lookup"><span data-stu-id="35aaa-110">PARAMETERS</span></span>

### <span data-ttu-id="35aaa-111">-Access</span><span class="sxs-lookup"><span data-stu-id="35aaa-111">-Access</span></span>
<span data-ttu-id="35aaa-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35aaa-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="35aaa-113">-DurationInSecond</span></span>
<span data-ttu-id="35aaa-114">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-114">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="35aaa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35aaa-115">-ResourceGroupName</span></span>
<span data-ttu-id="35aaa-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="35aaa-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="35aaa-117">-SnapshotName</span></span>
<span data-ttu-id="35aaa-118">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="35aaa-119">-확인</span><span class="sxs-lookup"><span data-stu-id="35aaa-119">-Confirm</span></span>
<span data-ttu-id="35aaa-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35aaa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35aaa-121">-WhatIf</span></span>
<span data-ttu-id="35aaa-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35aaa-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35aaa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35aaa-124">CommonParameters</span></span>
<span data-ttu-id="35aaa-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35aaa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35aaa-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35aaa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35aaa-127">입력</span><span class="sxs-lookup"><span data-stu-id="35aaa-127">INPUTS</span></span>

### <span data-ttu-id="35aaa-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35aaa-128">System.String</span></span>

## <span data-ttu-id="35aaa-129">출력</span><span class="sxs-lookup"><span data-stu-id="35aaa-129">OUTPUTS</span></span>

### <span data-ttu-id="35aaa-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="35aaa-130">System.Object</span></span>

## <span data-ttu-id="35aaa-131">상속자</span><span class="sxs-lookup"><span data-stu-id="35aaa-131">NOTES</span></span>

## <span data-ttu-id="35aaa-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35aaa-132">RELATED LINKS</span></span>

