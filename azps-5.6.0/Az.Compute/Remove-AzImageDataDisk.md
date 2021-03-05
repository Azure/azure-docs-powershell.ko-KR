---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983296"
---
# <span data-ttu-id="343c9-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="343c9-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="343c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="343c9-102">SYNOPSIS</span></span>
<span data-ttu-id="343c9-103">이미지 개체에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="343c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="343c9-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="343c9-105">DESCRIPTION</span></span>
<span data-ttu-id="343c9-106">**Remove-AzImageDataDisk** cmdlet은 이미지 개체에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="343c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="343c9-107">EXAMPLES</span></span>

### <span data-ttu-id="343c9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="343c9-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="343c9-109">이 명령은 'ResourceGroup01'의 기존 이미지 'Image01'에서 논리 단위 번호 1의 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="343c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="343c9-110">PARAMETERS</span></span>

### <span data-ttu-id="343c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343c9-111">-DefaultProfile</span></span>
<span data-ttu-id="343c9-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343c9-113">-Image</span><span class="sxs-lookup"><span data-stu-id="343c9-113">-Image</span></span>
<span data-ttu-id="343c9-114">로컬 이미지 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="343c9-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="343c9-115">-Lun</span></span>
<span data-ttu-id="343c9-116">LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="343c9-117">-확인</span><span class="sxs-lookup"><span data-stu-id="343c9-117">-Confirm</span></span>
<span data-ttu-id="343c9-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343c9-119">-WhatIf</span></span>
<span data-ttu-id="343c9-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="343c9-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343c9-122">CommonParameters</span></span>
<span data-ttu-id="343c9-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="343c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343c9-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="343c9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343c9-125">입력</span><span class="sxs-lookup"><span data-stu-id="343c9-125">INPUTS</span></span>

### <span data-ttu-id="343c9-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="343c9-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="343c9-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="343c9-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="343c9-128">출력</span><span class="sxs-lookup"><span data-stu-id="343c9-128">OUTPUTS</span></span>

### <span data-ttu-id="343c9-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="343c9-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="343c9-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="343c9-130">NOTES</span></span>

## <span data-ttu-id="343c9-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="343c9-131">RELATED LINKS</span></span>
