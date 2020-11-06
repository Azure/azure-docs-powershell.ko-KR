---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: ae45dadd2d5af2cf81a8735ca6725ee4798dbf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532090"
---
# <span data-ttu-id="20fab-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="20fab-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="20fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20fab-102">SYNOPSIS</span></span>
<span data-ttu-id="20fab-103">디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20fab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20fab-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20fab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20fab-105">DESCRIPTION</span></span>
<span data-ttu-id="20fab-106">**AzureRmDiskAccess** cmdlet은 디스크에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="20fab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20fab-107">EXAMPLES</span></span>

### <span data-ttu-id="20fab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="20fab-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="20fab-109">60 초 동안 리소스 그룹 ' ResourceGroup01 '의 ' Disk01 ' 디스크에 대 한 ' 읽기 ' 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="20fab-110">변수</span><span class="sxs-lookup"><span data-stu-id="20fab-110">PARAMETERS</span></span>

### <span data-ttu-id="20fab-111">-Access</span><span class="sxs-lookup"><span data-stu-id="20fab-111">-Access</span></span>
<span data-ttu-id="20fab-112">액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20fab-113">-AsJob</span></span>
<span data-ttu-id="20fab-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="20fab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fab-115">-DefaultProfile</span></span>
<span data-ttu-id="20fab-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20fab-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="20fab-117">-DiskName</span></span>
<span data-ttu-id="20fab-118">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="20fab-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="20fab-119">-DurationInSecond</span></span>
<span data-ttu-id="20fab-120">액세스 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fab-121">-ResourceGroupName</span></span>
<span data-ttu-id="20fab-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="20fab-123">-확인</span><span class="sxs-lookup"><span data-stu-id="20fab-123">-Confirm</span></span>
<span data-ttu-id="20fab-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20fab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20fab-125">-WhatIf</span></span>
<span data-ttu-id="20fab-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20fab-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20fab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fab-128">CommonParameters</span></span>
<span data-ttu-id="20fab-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fab-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fab-131">입력</span><span class="sxs-lookup"><span data-stu-id="20fab-131">INPUTS</span></span>

### <span data-ttu-id="20fab-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20fab-132">System.String</span></span>

## <span data-ttu-id="20fab-133">출력</span><span class="sxs-lookup"><span data-stu-id="20fab-133">OUTPUTS</span></span>

### <span data-ttu-id="20fab-134">Microsoft. i. m a. 모델. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="20fab-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="20fab-135">상속자</span><span class="sxs-lookup"><span data-stu-id="20fab-135">NOTES</span></span>

## <span data-ttu-id="20fab-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20fab-136">RELATED LINKS</span></span>
