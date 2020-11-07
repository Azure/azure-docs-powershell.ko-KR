---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b7e691d3bfea45fc8fc45725ddfe782418c12ab7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882309"
---
# <span data-ttu-id="3fe9b-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="3fe9b-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="3fe9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe9b-103">Image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fe9b-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fe9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3fe9b-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe9b-106">**AzureRmImageDataDisk** cmdlet은 image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="3fe9b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3fe9b-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe9b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fe9b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="3fe9b-109">이 명령은 리소스 그룹 ' ResourceGroup01 '의 기존 이미지 ' Image01 '에서 논리 단위 번호 1의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3fe9b-110">변수</span><span class="sxs-lookup"><span data-stu-id="3fe9b-110">PARAMETERS</span></span>

### <span data-ttu-id="3fe9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe9b-111">-DefaultProfile</span></span>
<span data-ttu-id="3fe9b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fe9b-113">-이미지</span><span class="sxs-lookup"><span data-stu-id="3fe9b-113">-Image</span></span>
<span data-ttu-id="3fe9b-114">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe9b-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="3fe9b-115">-Lun</span></span>
<span data-ttu-id="3fe9b-116">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe9b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="3fe9b-117">-Confirm</span></span>
<span data-ttu-id="3fe9b-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe9b-119">-WhatIf</span></span>
<span data-ttu-id="3fe9b-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fe9b-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe9b-122">CommonParameters</span></span>
<span data-ttu-id="3fe9b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe9b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe9b-125">입력</span><span class="sxs-lookup"><span data-stu-id="3fe9b-125">INPUTS</span></span>

### <span data-ttu-id="3fe9b-126">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="3fe9b-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="3fe9b-127">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="3fe9b-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3fe9b-128">출력</span><span class="sxs-lookup"><span data-stu-id="3fe9b-128">OUTPUTS</span></span>

### <span data-ttu-id="3fe9b-129">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="3fe9b-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="3fe9b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3fe9b-130">NOTES</span></span>

## <span data-ttu-id="3fe9b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fe9b-131">RELATED LINKS</span></span>

