---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213024"
---
# <span data-ttu-id="61d40-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d40-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="61d40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d40-102">SYNOPSIS</span></span>
<span data-ttu-id="61d40-103">CustomIpPrefix 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="61d40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61d40-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61d40-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61d40-105">DESCRIPTION</span></span>
<span data-ttu-id="61d40-106">**AzCustomIpPrefix** Cmdlet은 CustomIpPrefix 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="61d40-107">예제의</span><span class="sxs-lookup"><span data-stu-id="61d40-107">EXAMPLES</span></span>

### <span data-ttu-id="61d40-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="61d40-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="61d40-109">이 명령은 40.40.40.0/24의 cidr을 사용 하 여 리소스 그룹 $rgName에서 이름이 $prefixName 인 새 CustomIpPrefix 리소스를 만듭니다 westus</span><span class="sxs-lookup"><span data-stu-id="61d40-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="61d40-110">변수</span><span class="sxs-lookup"><span data-stu-id="61d40-110">PARAMETERS</span></span>

### <span data-ttu-id="61d40-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61d40-111">-AsJob</span></span>
<span data-ttu-id="61d40-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="61d40-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61d40-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="61d40-113">-Cidr</span></span>
<span data-ttu-id="61d40-114">CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="61d40-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d40-115">-DefaultProfile</span></span>
<span data-ttu-id="61d40-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-117">-위치</span><span class="sxs-lookup"><span data-stu-id="61d40-117">-Location</span></span>
<span data-ttu-id="61d40-118">CustomIpPrefix 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-119">-이름</span><span class="sxs-lookup"><span data-stu-id="61d40-119">-Name</span></span>
<span data-ttu-id="61d40-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d40-121">-ResourceGroupName</span></span>
<span data-ttu-id="61d40-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-123">태그</span><span class="sxs-lookup"><span data-stu-id="61d40-123">-Tag</span></span>
<span data-ttu-id="61d40-124">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="61d40-125">-Zone</span></span>
<span data-ttu-id="61d40-126">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d40-127">-확인</span><span class="sxs-lookup"><span data-stu-id="61d40-127">-Confirm</span></span>
<span data-ttu-id="61d40-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d40-129">-WhatIf</span></span>
<span data-ttu-id="61d40-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d40-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d40-132">CommonParameters</span></span>
<span data-ttu-id="61d40-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61d40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d40-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61d40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d40-135">입력</span><span class="sxs-lookup"><span data-stu-id="61d40-135">INPUTS</span></span>

### <span data-ttu-id="61d40-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61d40-136">System.String</span></span>

### <span data-ttu-id="61d40-137">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="61d40-137">System.String[]</span></span>

### <span data-ttu-id="61d40-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="61d40-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="61d40-139">출력</span><span class="sxs-lookup"><span data-stu-id="61d40-139">OUTPUTS</span></span>

### <span data-ttu-id="61d40-140">PSCustomIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="61d40-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="61d40-141">상속자</span><span class="sxs-lookup"><span data-stu-id="61d40-141">NOTES</span></span>

## <span data-ttu-id="61d40-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61d40-142">RELATED LINKS</span></span>

[<span data-ttu-id="61d40-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d40-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="61d40-144">제거-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d40-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="61d40-145">업데이트-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d40-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)