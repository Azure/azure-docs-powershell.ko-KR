---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344978"
---
# <span data-ttu-id="dc668-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="dc668-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="dc668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc668-102">SYNOPSIS</span></span>
<span data-ttu-id="dc668-103">디스크에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="dc668-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc668-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc668-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc668-105">DESCRIPTION</span></span>
<span data-ttu-id="dc668-106">**Revoke-AzDiskAccess** cmdlet은 디스크에 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="dc668-107">예제</span><span class="sxs-lookup"><span data-stu-id="dc668-107">EXAMPLES</span></span>

### <span data-ttu-id="dc668-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc668-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="dc668-109">'ResourceGroup01'이라는 리소스 그룹에서 'Disk01'이라는 디스크에 대한 액세스 권한을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="dc668-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc668-110">PARAMETERS</span></span>

### <span data-ttu-id="dc668-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc668-111">-AsJob</span></span>
<span data-ttu-id="dc668-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc668-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc668-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc668-113">-DefaultProfile</span></span>
<span data-ttu-id="dc668-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc668-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="dc668-115">-DiskName</span></span>
<span data-ttu-id="dc668-116">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="dc668-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc668-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc668-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dc668-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc668-119">-Confirm</span></span>
<span data-ttu-id="dc668-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc668-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc668-121">-WhatIf</span></span>
<span data-ttu-id="dc668-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc668-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc668-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc668-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc668-124">CommonParameters</span></span>
<span data-ttu-id="dc668-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc668-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc668-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc668-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc668-127">입력</span><span class="sxs-lookup"><span data-stu-id="dc668-127">INPUTS</span></span>

### <span data-ttu-id="dc668-128">System.String</span><span class="sxs-lookup"><span data-stu-id="dc668-128">System.String</span></span>

## <span data-ttu-id="dc668-129">출력</span><span class="sxs-lookup"><span data-stu-id="dc668-129">OUTPUTS</span></span>

### <span data-ttu-id="dc668-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dc668-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dc668-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc668-131">NOTES</span></span>

## <span data-ttu-id="dc668-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc668-132">RELATED LINKS</span></span>
