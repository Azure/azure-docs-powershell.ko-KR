---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535740"
---
# <span data-ttu-id="983e0-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="983e0-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="983e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="983e0-102">SYNOPSIS</span></span>
<span data-ttu-id="983e0-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="983e0-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="983e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="983e0-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="983e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="983e0-105">DESCRIPTION</span></span>
<span data-ttu-id="983e0-106">**AzureRmServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="983e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="983e0-107">EXAMPLES</span></span>

### <span data-ttu-id="983e0-108">예제 1: 이름을 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="983e0-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="983e0-109">이 명령은 이름이 "resourcegroup1" 인 resourcegroup에 속하는 이름 Policy1 인 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="983e0-110">예제 2: 입력 개체를 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="983e0-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="983e0-111">이 명령은 이름이 "resourcegroup1" 인 resourcegroup에 속하는 서비스 끝점 정책 개체 Policy1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="983e0-112">변수</span><span class="sxs-lookup"><span data-stu-id="983e0-112">PARAMETERS</span></span>

### <span data-ttu-id="983e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983e0-113">-DefaultProfile</span></span>
<span data-ttu-id="983e0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="983e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="983e0-115">-Force</span></span>
<span data-ttu-id="983e0-116">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="983e0-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="983e0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="983e0-117">-Name</span></span>
<span data-ttu-id="983e0-118">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983e0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="983e0-119">-PassThru</span></span>
<span data-ttu-id="983e0-120">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="983e0-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="983e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="983e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="983e0-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983e0-123">-확인</span><span class="sxs-lookup"><span data-stu-id="983e0-123">-Confirm</span></span>
<span data-ttu-id="983e0-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="983e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="983e0-125">-WhatIf</span></span>
<span data-ttu-id="983e0-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="983e0-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="983e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983e0-128">CommonParameters</span></span>
<span data-ttu-id="983e0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="983e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="983e0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983e0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983e0-131">입력</span><span class="sxs-lookup"><span data-stu-id="983e0-131">INPUTS</span></span>

### <span data-ttu-id="983e0-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="983e0-132">System.String</span></span>


## <span data-ttu-id="983e0-133">출력</span><span class="sxs-lookup"><span data-stu-id="983e0-133">OUTPUTS</span></span>

### <span data-ttu-id="983e0-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="983e0-134">System.Object</span></span>

## <span data-ttu-id="983e0-135">상속자</span><span class="sxs-lookup"><span data-stu-id="983e0-135">NOTES</span></span>

## <span data-ttu-id="983e0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="983e0-136">RELATED LINKS</span></span>
