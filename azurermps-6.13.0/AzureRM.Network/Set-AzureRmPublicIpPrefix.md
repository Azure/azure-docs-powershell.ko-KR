---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524351"
---
# <span data-ttu-id="46991-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46991-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="46991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46991-102">SYNOPSIS</span></span>
<span data-ttu-id="46991-103">기존 PublicIpPrefix에 대 한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="46991-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46991-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46991-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46991-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46991-105">DESCRIPTION</span></span>
<span data-ttu-id="46991-106">**AzureRmPublicIpPrefix** cmdlet은 공용 IP 접두사에 대 한 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46991-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="46991-107">예제의</span><span class="sxs-lookup"><span data-stu-id="46991-107">EXAMPLES</span></span>

### <span data-ttu-id="46991-108">공용 ip 접두사에 대 한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="46991-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="46991-109">첫 번째 명령은 기존 공용 IP 접두사를 가져오고, 두 번째 명령은 Tags 속성을 설정 하 고, 세 번째 명령은 기존 개체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="46991-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="46991-110">변수</span><span class="sxs-lookup"><span data-stu-id="46991-110">PARAMETERS</span></span>

### <span data-ttu-id="46991-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46991-111">-AsJob</span></span>
<span data-ttu-id="46991-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="46991-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46991-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46991-113">-DefaultProfile</span></span>
<span data-ttu-id="46991-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46991-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46991-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46991-115">-PublicIpPrefix</span></span>
<span data-ttu-id="46991-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="46991-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46991-117">-확인</span><span class="sxs-lookup"><span data-stu-id="46991-117">-Confirm</span></span>
<span data-ttu-id="46991-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46991-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46991-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46991-119">-WhatIf</span></span>
<span data-ttu-id="46991-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46991-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46991-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46991-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46991-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46991-122">CommonParameters</span></span>
<span data-ttu-id="46991-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46991-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="46991-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46991-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46991-125">입력</span><span class="sxs-lookup"><span data-stu-id="46991-125">INPUTS</span></span>

### <span data-ttu-id="46991-126">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="46991-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="46991-127">출력</span><span class="sxs-lookup"><span data-stu-id="46991-127">OUTPUTS</span></span>

### <span data-ttu-id="46991-128">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="46991-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="46991-129">상속자</span><span class="sxs-lookup"><span data-stu-id="46991-129">NOTES</span></span>

## <span data-ttu-id="46991-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46991-130">RELATED LINKS</span></span>
