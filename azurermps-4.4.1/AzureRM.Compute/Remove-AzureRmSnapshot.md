---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537380"
---
# <span data-ttu-id="ad3e9-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad3e9-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="ad3e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3e9-103">스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad3e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad3e9-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad3e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3e9-106">**제거-AzureRmSnapshot** cmdlet은 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="ad3e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad3e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad3e9-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="ad3e9-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Snapshot01 ' 인 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ad3e9-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad3e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ad3e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ad3e9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad3e9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ad3e9-113">-Force</span></span>
<span data-ttu-id="ad3e9-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad3e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad3e9-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad3e9-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ad3e9-117">-SnapshotName</span></span>
<span data-ttu-id="ad3e9-118">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ad3e9-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ad3e9-119">-Confirm</span></span>
<span data-ttu-id="ad3e9-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3e9-121">-WhatIf</span></span>
<span data-ttu-id="ad3e9-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3e9-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3e9-124">CommonParameters</span></span>
<span data-ttu-id="ad3e9-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3e9-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3e9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3e9-127">입력</span><span class="sxs-lookup"><span data-stu-id="ad3e9-127">INPUTS</span></span>

### <span data-ttu-id="ad3e9-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad3e9-128">System.String</span></span>

## <span data-ttu-id="ad3e9-129">출력</span><span class="sxs-lookup"><span data-stu-id="ad3e9-129">OUTPUTS</span></span>

### <span data-ttu-id="ad3e9-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ad3e9-130">System.Object</span></span>

## <span data-ttu-id="ad3e9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ad3e9-131">NOTES</span></span>

## <span data-ttu-id="ad3e9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad3e9-132">RELATED LINKS</span></span>

