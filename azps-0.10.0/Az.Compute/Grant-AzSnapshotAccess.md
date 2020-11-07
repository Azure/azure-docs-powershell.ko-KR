---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877023"
---
# <span data-ttu-id="8111e-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8111e-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="8111e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8111e-102">SYNOPSIS</span></span>
<span data-ttu-id="8111e-103">스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="8111e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8111e-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8111e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8111e-105">DESCRIPTION</span></span>
<span data-ttu-id="8111e-106">**AzSnapshotAccess** cmdlet은 스냅숏에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="8111e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8111e-107">EXAMPLES</span></span>

### <span data-ttu-id="8111e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8111e-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="8111e-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '에 ' Snapshot01 ' 이라는 스냅숏에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="8111e-110">변수</span><span class="sxs-lookup"><span data-stu-id="8111e-110">PARAMETERS</span></span>

### <span data-ttu-id="8111e-111">-Access</span><span class="sxs-lookup"><span data-stu-id="8111e-111">-Access</span></span>
<span data-ttu-id="8111e-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="8111e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8111e-113">-AsJob</span></span>
<span data-ttu-id="8111e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8111e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8111e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8111e-115">-DefaultProfile</span></span>
<span data-ttu-id="8111e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8111e-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="8111e-117">-DurationInSecond</span></span>
<span data-ttu-id="8111e-118">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="8111e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8111e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8111e-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8111e-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="8111e-121">-SnapshotName</span></span>
<span data-ttu-id="8111e-122">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="8111e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="8111e-123">-Confirm</span></span>
<span data-ttu-id="8111e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8111e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8111e-125">-WhatIf</span></span>
<span data-ttu-id="8111e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8111e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8111e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8111e-128">CommonParameters</span></span>
<span data-ttu-id="8111e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8111e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8111e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8111e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8111e-131">입력</span><span class="sxs-lookup"><span data-stu-id="8111e-131">INPUTS</span></span>

### <span data-ttu-id="8111e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8111e-132">System.String</span></span>

## <span data-ttu-id="8111e-133">출력</span><span class="sxs-lookup"><span data-stu-id="8111e-133">OUTPUTS</span></span>

### <span data-ttu-id="8111e-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="8111e-134">System.Object</span></span>

## <span data-ttu-id="8111e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="8111e-135">NOTES</span></span>

## <span data-ttu-id="8111e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8111e-136">RELATED LINKS</span></span>

