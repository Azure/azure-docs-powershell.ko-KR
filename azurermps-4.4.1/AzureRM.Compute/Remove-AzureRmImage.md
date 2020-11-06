---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536424"
---
# <span data-ttu-id="cf983-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="cf983-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="cf983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf983-102">SYNOPSIS</span></span>
<span data-ttu-id="cf983-103">이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf983-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf983-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf983-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf983-105">DESCRIPTION</span></span>
<span data-ttu-id="cf983-106">**AzureRmImage** cmdlet은 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="cf983-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cf983-107">EXAMPLES</span></span>

### <span data-ttu-id="cf983-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf983-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="cf983-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Image01 ' 인 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cf983-110">변수</span><span class="sxs-lookup"><span data-stu-id="cf983-110">PARAMETERS</span></span>

### <span data-ttu-id="cf983-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf983-111">-DefaultProfile</span></span>
<span data-ttu-id="cf983-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf983-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cf983-113">-Force</span></span>
<span data-ttu-id="cf983-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf983-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cf983-115">-ImageName</span></span>
<span data-ttu-id="cf983-116">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf983-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf983-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf983-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf983-119">-확인</span><span class="sxs-lookup"><span data-stu-id="cf983-119">-Confirm</span></span>
<span data-ttu-id="cf983-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf983-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf983-121">-WhatIf</span></span>
<span data-ttu-id="cf983-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf983-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf983-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf983-124">CommonParameters</span></span>
<span data-ttu-id="cf983-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf983-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf983-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf983-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf983-127">입력</span><span class="sxs-lookup"><span data-stu-id="cf983-127">INPUTS</span></span>

### <span data-ttu-id="cf983-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf983-128">System.String</span></span>

## <span data-ttu-id="cf983-129">출력</span><span class="sxs-lookup"><span data-stu-id="cf983-129">OUTPUTS</span></span>

### <span data-ttu-id="cf983-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="cf983-130">System.Object</span></span>

## <span data-ttu-id="cf983-131">상속자</span><span class="sxs-lookup"><span data-stu-id="cf983-131">NOTES</span></span>

## <span data-ttu-id="cf983-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf983-132">RELATED LINKS</span></span>

