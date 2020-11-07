---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872050"
---
# <span data-ttu-id="dfe68-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="dfe68-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="dfe68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe68-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe68-103">**테스트 AzPrivateLinkServiceVisibility** 는 현재 사용에 대해 개인 링크 서비스를 표시할지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="dfe68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfe68-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfe68-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe68-106">현재 사용에 대해 개인 링크 서비스를 표시할지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="dfe68-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfe68-107">EXAMPLES</span></span>

### <span data-ttu-id="dfe68-108">예제 1: contoso.cloudapp.azure.com을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="dfe68-109">변수</span><span class="sxs-lookup"><span data-stu-id="dfe68-109">PARAMETERS</span></span>

### <span data-ttu-id="dfe68-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe68-110">-DefaultProfile</span></span>
<span data-ttu-id="dfe68-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe68-112">-위치</span><span class="sxs-lookup"><span data-stu-id="dfe68-112">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe68-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="dfe68-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe68-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe68-114">-ResourceGroupName</span></span>
<span data-ttu-id="dfe68-115">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe68-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe68-116">CommonParameters</span></span>
<span data-ttu-id="dfe68-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfe68-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe68-118">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfe68-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe68-119">입력</span><span class="sxs-lookup"><span data-stu-id="dfe68-119">INPUTS</span></span>

### <span data-ttu-id="dfe68-120">않아야</span><span class="sxs-lookup"><span data-stu-id="dfe68-120">None</span></span>

## <span data-ttu-id="dfe68-121">출력</span><span class="sxs-lookup"><span data-stu-id="dfe68-121">OUTPUTS</span></span>

### <span data-ttu-id="dfe68-122">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dfe68-122">System.Boolean</span></span>

## <span data-ttu-id="dfe68-123">상속자</span><span class="sxs-lookup"><span data-stu-id="dfe68-123">NOTES</span></span>

## <span data-ttu-id="dfe68-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfe68-124">RELATED LINKS</span></span>
