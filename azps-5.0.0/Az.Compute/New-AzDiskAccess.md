---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309658"
---
# <span data-ttu-id="8975d-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8975d-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="8975d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8975d-102">SYNOPSIS</span></span>
<span data-ttu-id="8975d-103">디스크 액세스 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="8975d-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="8975d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8975d-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8975d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8975d-105">DESCRIPTION</span></span>
<span data-ttu-id="8975d-106">**AzDiskAccess** Cmdlet은 디스크 액세스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="8975d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8975d-107">EXAMPLES</span></span>

### <span data-ttu-id="8975d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8975d-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="8975d-109">이 명령은 지정 된 속성으로 디스크 접근을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="8975d-110">변수</span><span class="sxs-lookup"><span data-stu-id="8975d-110">PARAMETERS</span></span>

### <span data-ttu-id="8975d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8975d-111">-AsJob</span></span>
<span data-ttu-id="8975d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8975d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8975d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8975d-113">-DefaultProfile</span></span>
<span data-ttu-id="8975d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8975d-115">-위치</span><span class="sxs-lookup"><span data-stu-id="8975d-115">-Location</span></span>
<span data-ttu-id="8975d-116">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8975d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8975d-117">-Name</span></span>
<span data-ttu-id="8975d-118">디스크 액세스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8975d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8975d-119">-ResourceGroupName</span></span>
<span data-ttu-id="8975d-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8975d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8975d-121">-Confirm</span></span>
<span data-ttu-id="8975d-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8975d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8975d-123">-WhatIf</span></span>
<span data-ttu-id="8975d-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8975d-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8975d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8975d-126">CommonParameters</span></span>
<span data-ttu-id="8975d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8975d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8975d-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8975d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8975d-129">입력</span><span class="sxs-lookup"><span data-stu-id="8975d-129">INPUTS</span></span>

### <span data-ttu-id="8975d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8975d-130">System.String</span></span>

## <span data-ttu-id="8975d-131">출력</span><span class="sxs-lookup"><span data-stu-id="8975d-131">OUTPUTS</span></span>

### <span data-ttu-id="8975d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8975d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8975d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8975d-133">NOTES</span></span>

## <span data-ttu-id="8975d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8975d-134">RELATED LINKS</span></span>
