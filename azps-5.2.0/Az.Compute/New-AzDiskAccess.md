---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364932"
---
# <span data-ttu-id="c73a3-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c73a3-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="c73a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c73a3-103">디스크 액세스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="c73a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="c73a3-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73a3-105">설명</span><span class="sxs-lookup"><span data-stu-id="c73a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c73a3-106">**New-AzDiskAccess** cmdlet은 디스크 액세스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="c73a3-107">예제</span><span class="sxs-lookup"><span data-stu-id="c73a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c73a3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c73a3-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="c73a3-109">이 명령은 주어진 속성을 사용하여 디스크 액세스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="c73a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73a3-110">PARAMETERS</span></span>

### <span data-ttu-id="c73a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c73a3-111">-AsJob</span></span>
<span data-ttu-id="c73a3-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c73a3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c73a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73a3-113">-DefaultProfile</span></span>
<span data-ttu-id="c73a3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c73a3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c73a3-115">-Location</span></span>
<span data-ttu-id="c73a3-116">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-116">Specifies the location.</span></span>

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

### <span data-ttu-id="c73a3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c73a3-117">-Name</span></span>
<span data-ttu-id="c73a3-118">디스크 액세스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="c73a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c73a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="c73a3-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c73a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c73a3-121">-Confirm</span></span>
<span data-ttu-id="c73a3-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73a3-123">-WhatIf</span></span>
<span data-ttu-id="c73a3-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c73a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73a3-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73a3-126">CommonParameters</span></span>
<span data-ttu-id="c73a3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c73a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73a3-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c73a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73a3-129">입력</span><span class="sxs-lookup"><span data-stu-id="c73a3-129">INPUTS</span></span>

### <span data-ttu-id="c73a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c73a3-130">System.String</span></span>

## <span data-ttu-id="c73a3-131">출력</span><span class="sxs-lookup"><span data-stu-id="c73a3-131">OUTPUTS</span></span>

### <span data-ttu-id="c73a3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c73a3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="c73a3-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c73a3-133">NOTES</span></span>

## <span data-ttu-id="c73a3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c73a3-134">RELATED LINKS</span></span>
