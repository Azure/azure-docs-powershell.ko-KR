---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882001"
---
# <span data-ttu-id="a5e77-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a5e77-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="a5e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e77-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e77-103">디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5e77-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5e77-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e77-106">**AzureRmDiskAccess** cmdlet은 디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="a5e77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5e77-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5e77-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="a5e77-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '의 ' Disk01 ' 디스크에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="a5e77-110">변수</span><span class="sxs-lookup"><span data-stu-id="a5e77-110">PARAMETERS</span></span>

### <span data-ttu-id="a5e77-111">-Access</span><span class="sxs-lookup"><span data-stu-id="a5e77-111">-Access</span></span>
<span data-ttu-id="a5e77-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="a5e77-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5e77-113">-AsJob</span></span>
<span data-ttu-id="a5e77-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5e77-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5e77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e77-115">-DefaultProfile</span></span>
<span data-ttu-id="a5e77-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e77-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a5e77-117">-DiskName</span></span>
<span data-ttu-id="a5e77-118">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a5e77-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="a5e77-119">-DurationInSecond</span></span>
<span data-ttu-id="a5e77-120">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="a5e77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e77-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5e77-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a5e77-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a5e77-123">-Confirm</span></span>
<span data-ttu-id="a5e77-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e77-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e77-125">-WhatIf</span></span>
<span data-ttu-id="a5e77-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5e77-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e77-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e77-128">CommonParameters</span></span>
<span data-ttu-id="a5e77-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e77-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e77-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e77-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e77-131">입력</span><span class="sxs-lookup"><span data-stu-id="a5e77-131">INPUTS</span></span>

### <span data-ttu-id="a5e77-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5e77-132">System.String</span></span>

## <span data-ttu-id="a5e77-133">출력</span><span class="sxs-lookup"><span data-stu-id="a5e77-133">OUTPUTS</span></span>

### <span data-ttu-id="a5e77-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a5e77-134">System.Object</span></span>

## <span data-ttu-id="a5e77-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a5e77-135">NOTES</span></span>

## <span data-ttu-id="a5e77-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5e77-136">RELATED LINKS</span></span>

