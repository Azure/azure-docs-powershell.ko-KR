---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 5fe22889443d38e10cff061008c4ed2582825887
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876970"
---
# <span data-ttu-id="c0619-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="c0619-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="c0619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0619-102">SYNOPSIS</span></span>
<span data-ttu-id="c0619-103">스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-103">Removes a snapshot.</span></span>

## <span data-ttu-id="c0619-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0619-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0619-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c0619-105">DESCRIPTION</span></span>
<span data-ttu-id="c0619-106">**제거-AzSnapshot** cmdlet은 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="c0619-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c0619-107">EXAMPLES</span></span>

### <span data-ttu-id="c0619-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0619-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="c0619-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Snapshot01 ' 인 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c0619-110">변수</span><span class="sxs-lookup"><span data-stu-id="c0619-110">PARAMETERS</span></span>

### <span data-ttu-id="c0619-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0619-111">-AsJob</span></span>
<span data-ttu-id="c0619-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0619-113">-DefaultProfile</span></span>
<span data-ttu-id="c0619-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0619-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0619-115">-Force</span></span>
<span data-ttu-id="c0619-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0619-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0619-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0619-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c0619-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c0619-119">-SnapshotName</span></span>
<span data-ttu-id="c0619-120">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c0619-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c0619-121">-Confirm</span></span>
<span data-ttu-id="c0619-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0619-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0619-123">-WhatIf</span></span>
<span data-ttu-id="c0619-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0619-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0619-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0619-126">CommonParameters</span></span>
<span data-ttu-id="c0619-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0619-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0619-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0619-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0619-129">입력</span><span class="sxs-lookup"><span data-stu-id="c0619-129">INPUTS</span></span>

### <span data-ttu-id="c0619-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0619-130">System.String</span></span>

## <span data-ttu-id="c0619-131">출력</span><span class="sxs-lookup"><span data-stu-id="c0619-131">OUTPUTS</span></span>

### <span data-ttu-id="c0619-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c0619-132">System.Object</span></span>

## <span data-ttu-id="c0619-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c0619-133">NOTES</span></span>

## <span data-ttu-id="c0619-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0619-134">RELATED LINKS</span></span>

