---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881114"
---
# <span data-ttu-id="ba154-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba154-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="ba154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba154-102">SYNOPSIS</span></span>
<span data-ttu-id="ba154-103">디스크에 대 한 액세스 권한을 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba154-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba154-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba154-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba154-105">DESCRIPTION</span></span>
<span data-ttu-id="ba154-106">AzureRmDiskAccess cmdlet은 디스크에 대 한 액세스를 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="ba154-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba154-107">EXAMPLES</span></span>

### <span data-ttu-id="ba154-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba154-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="ba154-109">리소스 그룹 ' ResourceGroup01 '의 ' Disk01 ' 디스크에 대 한 액세스 권한을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ba154-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba154-110">PARAMETERS</span></span>

### <span data-ttu-id="ba154-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba154-111">-AsJob</span></span>
<span data-ttu-id="ba154-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ba154-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba154-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba154-113">-DefaultProfile</span></span>
<span data-ttu-id="ba154-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba154-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ba154-115">-DiskName</span></span>
<span data-ttu-id="ba154-116">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ba154-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba154-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba154-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba154-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ba154-119">-Confirm</span></span>
<span data-ttu-id="ba154-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba154-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba154-121">-WhatIf</span></span>
<span data-ttu-id="ba154-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba154-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba154-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba154-124">CommonParameters</span></span>
<span data-ttu-id="ba154-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba154-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba154-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba154-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba154-127">입력</span><span class="sxs-lookup"><span data-stu-id="ba154-127">INPUTS</span></span>

### <span data-ttu-id="ba154-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba154-128">System.String</span></span>

## <span data-ttu-id="ba154-129">출력</span><span class="sxs-lookup"><span data-stu-id="ba154-129">OUTPUTS</span></span>

### <span data-ttu-id="ba154-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ba154-130">System.Object</span></span>

## <span data-ttu-id="ba154-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ba154-131">NOTES</span></span>

## <span data-ttu-id="ba154-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba154-132">RELATED LINKS</span></span>
