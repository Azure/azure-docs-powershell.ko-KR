---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874991"
---
# <span data-ttu-id="519c5-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="519c5-101">New-AzsIpPool</span></span>

## <span data-ttu-id="519c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="519c5-102">SYNOPSIS</span></span>
<span data-ttu-id="519c5-103">인프라 IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="519c5-104">만든 후에는 IP 풀을 삭제 하거나 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="519c5-105">구문과</span><span class="sxs-lookup"><span data-stu-id="519c5-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="519c5-106">설명은</span><span class="sxs-lookup"><span data-stu-id="519c5-106">DESCRIPTION</span></span>
<span data-ttu-id="519c5-107">인프라 IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="519c5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="519c5-108">EXAMPLES</span></span>

### <span data-ttu-id="519c5-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="519c5-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="519c5-110">새 IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-110">Create a new IP pool.</span></span>

## <span data-ttu-id="519c5-111">변수</span><span class="sxs-lookup"><span data-stu-id="519c5-111">PARAMETERS</span></span>

### <span data-ttu-id="519c5-112">-이름</span><span class="sxs-lookup"><span data-stu-id="519c5-112">-Name</span></span>
<span data-ttu-id="519c5-113">IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-113">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="519c5-114">-AddressPrefix</span></span>
<span data-ttu-id="519c5-115">주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-115">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="519c5-116">-StartIpAddress</span></span>
<span data-ttu-id="519c5-117">시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-117">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="519c5-118">-EndIpAddress</span></span>
<span data-ttu-id="519c5-119">끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-119">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-120">-위치</span><span class="sxs-lookup"><span data-stu-id="519c5-120">-Location</span></span>
<span data-ttu-id="519c5-121">리소스가 있는 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-121">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="519c5-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-124">태그</span><span class="sxs-lookup"><span data-stu-id="519c5-124">-Tags</span></span>
<span data-ttu-id="519c5-125">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-125">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="519c5-126">-AsJob</span></span>
<span data-ttu-id="519c5-127">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-127">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="519c5-128">-WhatIf</span></span>
<span data-ttu-id="519c5-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="519c5-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="519c5-131">-확인</span><span class="sxs-lookup"><span data-stu-id="519c5-131">-Confirm</span></span>
<span data-ttu-id="519c5-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="519c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519c5-133">CommonParameters</span></span>
<span data-ttu-id="519c5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="519c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519c5-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="519c5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519c5-136">입력</span><span class="sxs-lookup"><span data-stu-id="519c5-136">INPUTS</span></span>

## <span data-ttu-id="519c5-137">출력</span><span class="sxs-lookup"><span data-stu-id="519c5-137">OUTPUTS</span></span>

### <span data-ttu-id="519c5-138">ProvisioningState. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="519c5-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="519c5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="519c5-139">NOTES</span></span>

## <span data-ttu-id="519c5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="519c5-140">RELATED LINKS</span></span>
