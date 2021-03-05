---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 709fab1ab8ba39193ef9831cd03d7b1cd53208dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001771"
---
# <span data-ttu-id="90ab5-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="90ab5-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="90ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="90ab5-103">디스크에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="90ab5-104">구문</span><span class="sxs-lookup"><span data-stu-id="90ab5-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90ab5-105">설명</span><span class="sxs-lookup"><span data-stu-id="90ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="90ab5-106">**Grant-AzDiskAccess** cmdlet은 디스크에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="90ab5-107">예제</span><span class="sxs-lookup"><span data-stu-id="90ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="90ab5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90ab5-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="90ab5-109">'ResourceGroup01'이라는 리소스 그룹의 'Disk01'이라는 디스크에 60초 동안 '읽기' 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="90ab5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="90ab5-111">-Access</span><span class="sxs-lookup"><span data-stu-id="90ab5-111">-Access</span></span>
<span data-ttu-id="90ab5-112">액세스 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="90ab5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90ab5-113">-AsJob</span></span>
<span data-ttu-id="90ab5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="90ab5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="90ab5-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ab5-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="90ab5-117">-DiskName</span></span>
<span data-ttu-id="90ab5-118">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="90ab5-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="90ab5-119">-DurationInSecond</span></span>
<span data-ttu-id="90ab5-120">몇 초 만에 액세스 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="90ab5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ab5-121">-ResourceGroupName</span></span>
<span data-ttu-id="90ab5-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90ab5-123">-확인</span><span class="sxs-lookup"><span data-stu-id="90ab5-123">-Confirm</span></span>
<span data-ttu-id="90ab5-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ab5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ab5-125">-WhatIf</span></span>
<span data-ttu-id="90ab5-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90ab5-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ab5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ab5-128">CommonParameters</span></span>
<span data-ttu-id="90ab5-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90ab5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ab5-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90ab5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ab5-131">입력</span><span class="sxs-lookup"><span data-stu-id="90ab5-131">INPUTS</span></span>

### <span data-ttu-id="90ab5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="90ab5-132">System.String</span></span>

## <span data-ttu-id="90ab5-133">출력</span><span class="sxs-lookup"><span data-stu-id="90ab5-133">OUTPUTS</span></span>

### <span data-ttu-id="90ab5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="90ab5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="90ab5-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90ab5-135">NOTES</span></span>

## <span data-ttu-id="90ab5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90ab5-136">RELATED LINKS</span></span>
