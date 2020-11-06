---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526952"
---
# <span data-ttu-id="645ba-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="645ba-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="645ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="645ba-102">SYNOPSIS</span></span>
<span data-ttu-id="645ba-103">디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="645ba-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="645ba-105">DESCRIPTION</span></span>
<span data-ttu-id="645ba-106">**AzureRmDiskAccess** cmdlet은 디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="645ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="645ba-107">EXAMPLES</span></span>

### <span data-ttu-id="645ba-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="645ba-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="645ba-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '의 ' Disk01 ' 디스크에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="645ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="645ba-110">PARAMETERS</span></span>

### <span data-ttu-id="645ba-111">-Access</span><span class="sxs-lookup"><span data-stu-id="645ba-111">-Access</span></span>
<span data-ttu-id="645ba-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645ba-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="645ba-113">-DiskName</span></span>
<span data-ttu-id="645ba-114">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="645ba-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="645ba-115">-DurationInSecond</span></span>
<span data-ttu-id="645ba-116">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-116">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="645ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="645ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="645ba-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="645ba-119">-확인</span><span class="sxs-lookup"><span data-stu-id="645ba-119">-Confirm</span></span>
<span data-ttu-id="645ba-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645ba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645ba-121">-WhatIf</span></span>
<span data-ttu-id="645ba-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="645ba-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645ba-124">CommonParameters</span></span>
<span data-ttu-id="645ba-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="645ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645ba-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645ba-127">입력</span><span class="sxs-lookup"><span data-stu-id="645ba-127">INPUTS</span></span>

### <span data-ttu-id="645ba-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="645ba-128">System.String</span></span>

## <span data-ttu-id="645ba-129">출력</span><span class="sxs-lookup"><span data-stu-id="645ba-129">OUTPUTS</span></span>

### <span data-ttu-id="645ba-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="645ba-130">System.Object</span></span>

## <span data-ttu-id="645ba-131">상속자</span><span class="sxs-lookup"><span data-stu-id="645ba-131">NOTES</span></span>

## <span data-ttu-id="645ba-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="645ba-132">RELATED LINKS</span></span>

