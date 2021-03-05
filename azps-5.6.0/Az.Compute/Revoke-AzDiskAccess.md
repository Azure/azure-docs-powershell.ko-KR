---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 767104edb73265f472e155e8d003b0b5e96906e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963227"
---
# <span data-ttu-id="be8ac-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="be8ac-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="be8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="be8ac-103">디스크에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="be8ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="be8ac-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be8ac-105">설명</span><span class="sxs-lookup"><span data-stu-id="be8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="be8ac-106">**Revoke-AzDiskAccess** cmdlet은 디스크에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="be8ac-107">예제</span><span class="sxs-lookup"><span data-stu-id="be8ac-107">EXAMPLES</span></span>

### <span data-ttu-id="be8ac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="be8ac-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="be8ac-109">'ResourceGroup01'이라는 리소스 그룹의 'Disk01'이라는 디스크에 대한 액세스 해지</span><span class="sxs-lookup"><span data-stu-id="be8ac-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="be8ac-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="be8ac-110">PARAMETERS</span></span>

### <span data-ttu-id="be8ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be8ac-111">-AsJob</span></span>
<span data-ttu-id="be8ac-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="be8ac-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be8ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8ac-113">-DefaultProfile</span></span>
<span data-ttu-id="be8ac-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be8ac-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="be8ac-115">-DiskName</span></span>
<span data-ttu-id="be8ac-116">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="be8ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="be8ac-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="be8ac-119">-확인</span><span class="sxs-lookup"><span data-stu-id="be8ac-119">-Confirm</span></span>
<span data-ttu-id="be8ac-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8ac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8ac-121">-WhatIf</span></span>
<span data-ttu-id="be8ac-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be8ac-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8ac-124">CommonParameters</span></span>
<span data-ttu-id="be8ac-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8ac-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be8ac-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8ac-127">입력</span><span class="sxs-lookup"><span data-stu-id="be8ac-127">INPUTS</span></span>

### <span data-ttu-id="be8ac-128">System.String</span><span class="sxs-lookup"><span data-stu-id="be8ac-128">System.String</span></span>

## <span data-ttu-id="be8ac-129">출력</span><span class="sxs-lookup"><span data-stu-id="be8ac-129">OUTPUTS</span></span>

### <span data-ttu-id="be8ac-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="be8ac-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="be8ac-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="be8ac-131">NOTES</span></span>

## <span data-ttu-id="be8ac-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be8ac-132">RELATED LINKS</span></span>
