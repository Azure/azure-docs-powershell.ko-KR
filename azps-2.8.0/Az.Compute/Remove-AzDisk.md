---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 46cbb87d54d1eb80857d3d0fbc786cb8296f4ac0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697331"
---
# <span data-ttu-id="43056-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="43056-101">Remove-AzDisk</span></span>

## <span data-ttu-id="43056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43056-102">SYNOPSIS</span></span>
<span data-ttu-id="43056-103">디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-103">Removes a disk.</span></span>

## <span data-ttu-id="43056-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43056-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43056-105">설명은</span><span class="sxs-lookup"><span data-stu-id="43056-105">DESCRIPTION</span></span>
<span data-ttu-id="43056-106">**AzDisk** cmdlet이 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="43056-107">예제의</span><span class="sxs-lookup"><span data-stu-id="43056-107">EXAMPLES</span></span>

### <span data-ttu-id="43056-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="43056-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="43056-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="43056-110">변수</span><span class="sxs-lookup"><span data-stu-id="43056-110">PARAMETERS</span></span>

### <span data-ttu-id="43056-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43056-111">-AsJob</span></span>
<span data-ttu-id="43056-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="43056-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43056-113">-DefaultProfile</span></span>
<span data-ttu-id="43056-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43056-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43056-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="43056-115">-DiskName</span></span>
<span data-ttu-id="43056-116">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="43056-117">-Force</span><span class="sxs-lookup"><span data-stu-id="43056-117">-Force</span></span>
<span data-ttu-id="43056-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43056-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43056-119">-ResourceGroupName</span></span>
<span data-ttu-id="43056-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="43056-121">-확인</span><span class="sxs-lookup"><span data-stu-id="43056-121">-Confirm</span></span>
<span data-ttu-id="43056-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43056-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43056-123">-WhatIf</span></span>
<span data-ttu-id="43056-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43056-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43056-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43056-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43056-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43056-126">CommonParameters</span></span>
<span data-ttu-id="43056-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43056-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43056-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43056-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43056-129">입력</span><span class="sxs-lookup"><span data-stu-id="43056-129">INPUTS</span></span>

### <span data-ttu-id="43056-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43056-130">System.String</span></span>

## <span data-ttu-id="43056-131">출력</span><span class="sxs-lookup"><span data-stu-id="43056-131">OUTPUTS</span></span>

### <span data-ttu-id="43056-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="43056-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="43056-133">상속자</span><span class="sxs-lookup"><span data-stu-id="43056-133">NOTES</span></span>

## <span data-ttu-id="43056-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43056-134">RELATED LINKS</span></span>