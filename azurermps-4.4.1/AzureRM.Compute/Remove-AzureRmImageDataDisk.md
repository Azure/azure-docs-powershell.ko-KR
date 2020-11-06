---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 1d37af16fcb84db8247ac5db495abb1f41319c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536423"
---
# <span data-ttu-id="f5ece-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5ece-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="f5ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ece-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ece-103">Image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ece-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5ece-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ece-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5ece-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ece-106">**AzureRmImageDataDisk** cmdlet은 image 개체에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="f5ece-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5ece-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ece-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5ece-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="f5ece-109">이 명령은 리소스 그룹 ' ResourceGroup01 '의 기존 이미지 ' Image01 '에서 논리 단위 번호 1의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f5ece-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5ece-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ece-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ece-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ece-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ece-113">-이미지</span><span class="sxs-lookup"><span data-stu-id="f5ece-113">-Image</span></span>
<span data-ttu-id="f5ece-114">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ece-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="f5ece-115">-Lun</span></span>
<span data-ttu-id="f5ece-116">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ece-117">-확인</span><span class="sxs-lookup"><span data-stu-id="f5ece-117">-Confirm</span></span>
<span data-ttu-id="f5ece-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ece-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ece-119">-WhatIf</span></span>
<span data-ttu-id="f5ece-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5ece-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ece-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ece-122">CommonParameters</span></span>
<span data-ttu-id="f5ece-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ece-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ece-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ece-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ece-125">입력</span><span class="sxs-lookup"><span data-stu-id="f5ece-125">INPUTS</span></span>

### <span data-ttu-id="f5ece-126">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="f5ece-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="f5ece-127">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="f5ece-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f5ece-128">출력</span><span class="sxs-lookup"><span data-stu-id="f5ece-128">OUTPUTS</span></span>

### <span data-ttu-id="f5ece-129">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="f5ece-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="f5ece-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f5ece-130">NOTES</span></span>

## <span data-ttu-id="f5ece-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5ece-131">RELATED LINKS</span></span>

