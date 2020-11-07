---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 6fe1fee57942c72b51382b6332df22993a9bb56e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868926"
---
# <span data-ttu-id="d8004-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d8004-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="d8004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8004-102">SYNOPSIS</span></span>
<span data-ttu-id="d8004-103">디스크에 대 한 액세스 권한을 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="d8004-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8004-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8004-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8004-105">DESCRIPTION</span></span>
<span data-ttu-id="d8004-106">AzDiskAccess cmdlet은 디스크에 대 한 액세스를 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="d8004-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8004-107">EXAMPLES</span></span>

### <span data-ttu-id="d8004-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8004-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="d8004-109">리소스 그룹 ' ResourceGroup01 '의 ' Disk01 ' 디스크에 대 한 액세스 권한을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="d8004-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8004-110">PARAMETERS</span></span>

### <span data-ttu-id="d8004-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8004-111">-AsJob</span></span>
<span data-ttu-id="d8004-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8004-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8004-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8004-113">-DefaultProfile</span></span>
<span data-ttu-id="d8004-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8004-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d8004-115">-DiskName</span></span>
<span data-ttu-id="d8004-116">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="d8004-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8004-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8004-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8004-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d8004-119">-Confirm</span></span>
<span data-ttu-id="d8004-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8004-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8004-121">-WhatIf</span></span>
<span data-ttu-id="d8004-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8004-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8004-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8004-124">CommonParameters</span></span>
<span data-ttu-id="d8004-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8004-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8004-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8004-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8004-127">입력</span><span class="sxs-lookup"><span data-stu-id="d8004-127">INPUTS</span></span>

### <span data-ttu-id="d8004-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8004-128">System.String</span></span>

## <span data-ttu-id="d8004-129">출력</span><span class="sxs-lookup"><span data-stu-id="d8004-129">OUTPUTS</span></span>

### <span data-ttu-id="d8004-130">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="d8004-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d8004-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d8004-131">NOTES</span></span>

## <span data-ttu-id="d8004-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8004-132">RELATED LINKS</span></span>
