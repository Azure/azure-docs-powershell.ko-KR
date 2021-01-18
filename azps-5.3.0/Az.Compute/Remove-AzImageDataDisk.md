---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496003"
---
# <span data-ttu-id="b8fc2-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="b8fc2-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="b8fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fc2-103">이미지 개체에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="b8fc2-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8fc2-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fc2-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fc2-106">**Remove-AzImageDataDisk** cmdlet은 이미지 개체에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="b8fc2-107">예제</span><span class="sxs-lookup"><span data-stu-id="b8fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="b8fc2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8fc2-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="b8fc2-109">이 명령은 리소스 그룹 'ResourceGroup01'의 기존 이미지 'Image01'에서 논리 단위 번호 1의 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b8fc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="b8fc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fc2-111">-DefaultProfile</span></span>
<span data-ttu-id="b8fc2-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8fc2-113">-Image</span><span class="sxs-lookup"><span data-stu-id="b8fc2-113">-Image</span></span>
<span data-ttu-id="b8fc2-114">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="b8fc2-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="b8fc2-115">-Lun</span></span>
<span data-ttu-id="b8fc2-116">LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="b8fc2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8fc2-117">-Confirm</span></span>
<span data-ttu-id="b8fc2-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fc2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fc2-119">-WhatIf</span></span>
<span data-ttu-id="b8fc2-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b8fc2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8fc2-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fc2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fc2-122">CommonParameters</span></span>
<span data-ttu-id="b8fc2-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fc2-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8fc2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fc2-125">입력</span><span class="sxs-lookup"><span data-stu-id="b8fc2-125">INPUTS</span></span>

### <span data-ttu-id="b8fc2-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="b8fc2-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="b8fc2-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8fc2-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b8fc2-128">출력</span><span class="sxs-lookup"><span data-stu-id="b8fc2-128">OUTPUTS</span></span>

### <span data-ttu-id="b8fc2-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="b8fc2-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b8fc2-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8fc2-130">NOTES</span></span>

## <span data-ttu-id="b8fc2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8fc2-131">RELATED LINKS</span></span>
