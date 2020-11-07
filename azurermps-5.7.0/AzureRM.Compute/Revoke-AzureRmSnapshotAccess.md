---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711186"
---
# <span data-ttu-id="e62ba-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e62ba-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="e62ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e62ba-103">스냅숏에 대 한 액세스 권한을 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e62ba-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e62ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e62ba-105">DESCRIPTION</span></span>
<span data-ttu-id="e62ba-106">AzureRmSnapshotAccess cmdlet은 스냅숏에 대 한 액세스 권한을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="e62ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e62ba-107">EXAMPLES</span></span>

### <span data-ttu-id="e62ba-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e62ba-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="e62ba-109">리소스 그룹 ' ResourceGroup01 '에서 ' Snapshot01 ' 이라는 스냅숏에 대 한 액세스 권한을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e62ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="e62ba-110">PARAMETERS</span></span>

### <span data-ttu-id="e62ba-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62ba-111">-ResourceGroupName</span></span>
<span data-ttu-id="e62ba-112">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e62ba-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e62ba-113">-SnapshotName</span></span>
<span data-ttu-id="e62ba-114">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="e62ba-115">-확인</span><span class="sxs-lookup"><span data-stu-id="e62ba-115">-Confirm</span></span>
<span data-ttu-id="e62ba-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62ba-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62ba-117">-WhatIf</span></span>
<span data-ttu-id="e62ba-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e62ba-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62ba-120">CommonParameters</span></span>
<span data-ttu-id="e62ba-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62ba-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62ba-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62ba-123">입력</span><span class="sxs-lookup"><span data-stu-id="e62ba-123">INPUTS</span></span>

### <span data-ttu-id="e62ba-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e62ba-124">System.String</span></span>

## <span data-ttu-id="e62ba-125">출력</span><span class="sxs-lookup"><span data-stu-id="e62ba-125">OUTPUTS</span></span>

### <span data-ttu-id="e62ba-126">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e62ba-126">System.Object</span></span>

## <span data-ttu-id="e62ba-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e62ba-127">NOTES</span></span>

## <span data-ttu-id="e62ba-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e62ba-128">RELATED LINKS</span></span>

