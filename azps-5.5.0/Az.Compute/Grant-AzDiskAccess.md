---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210061"
---
# <span data-ttu-id="b1dac-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b1dac-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="b1dac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1dac-102">SYNOPSIS</span></span>
<span data-ttu-id="b1dac-103">디스크에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="b1dac-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1dac-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1dac-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1dac-105">DESCRIPTION</span></span>
<span data-ttu-id="b1dac-106">**Grant-AzDiskAccess** cmdlet은 디스크에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="b1dac-107">예제</span><span class="sxs-lookup"><span data-stu-id="b1dac-107">EXAMPLES</span></span>

### <span data-ttu-id="b1dac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1dac-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="b1dac-109">60초 동안 'ResourceGroup01'이라는 리소스 그룹의 'Disk01'이라는 디스크에 '읽기' 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="b1dac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1dac-110">PARAMETERS</span></span>

### <span data-ttu-id="b1dac-111">-Access</span><span class="sxs-lookup"><span data-stu-id="b1dac-111">-Access</span></span>
<span data-ttu-id="b1dac-112">액세스 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1dac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1dac-113">-AsJob</span></span>
<span data-ttu-id="b1dac-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b1dac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1dac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1dac-115">-DefaultProfile</span></span>
<span data-ttu-id="b1dac-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1dac-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b1dac-117">-DiskName</span></span>
<span data-ttu-id="b1dac-118">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1dac-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="b1dac-119">-DurationInSecond</span></span>
<span data-ttu-id="b1dac-120">액세스 기간을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1dac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1dac-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1dac-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1dac-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1dac-123">-Confirm</span></span>
<span data-ttu-id="b1dac-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1dac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1dac-125">-WhatIf</span></span>
<span data-ttu-id="b1dac-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1dac-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1dac-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1dac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1dac-128">CommonParameters</span></span>
<span data-ttu-id="b1dac-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1dac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1dac-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1dac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1dac-131">입력</span><span class="sxs-lookup"><span data-stu-id="b1dac-131">INPUTS</span></span>

### <span data-ttu-id="b1dac-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b1dac-132">System.String</span></span>

## <span data-ttu-id="b1dac-133">출력</span><span class="sxs-lookup"><span data-stu-id="b1dac-133">OUTPUTS</span></span>

### <span data-ttu-id="b1dac-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="b1dac-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="b1dac-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1dac-135">NOTES</span></span>

## <span data-ttu-id="b1dac-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1dac-136">RELATED LINKS</span></span>
