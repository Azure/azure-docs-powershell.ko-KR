---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951712"
---
# <span data-ttu-id="83b01-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="83b01-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="83b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b01-102">SYNOPSIS</span></span>
<span data-ttu-id="83b01-103">**Test-AzPrivateLinkServiceVisibility는** 개인 링크 서비스가 현재 사용에 대해 표시되는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="83b01-104">구문</span><span class="sxs-lookup"><span data-stu-id="83b01-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83b01-105">설명</span><span class="sxs-lookup"><span data-stu-id="83b01-105">DESCRIPTION</span></span>
<span data-ttu-id="83b01-106">현재 사용에 대해 개인 링크 서비스가 표시되는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="83b01-107">예제</span><span class="sxs-lookup"><span data-stu-id="83b01-107">EXAMPLES</span></span>

### <span data-ttu-id="83b01-108">예제 1: contoso.cloudapp.azure.com 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="83b01-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83b01-109">PARAMETERS</span></span>

### <span data-ttu-id="83b01-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b01-110">-DefaultProfile</span></span>
<span data-ttu-id="83b01-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b01-112">-Location</span><span class="sxs-lookup"><span data-stu-id="83b01-112">-Location</span></span>
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

### <span data-ttu-id="83b01-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="83b01-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="83b01-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b01-114">-ResourceGroupName</span></span>
<span data-ttu-id="83b01-115">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="83b01-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b01-116">CommonParameters</span></span>
<span data-ttu-id="83b01-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83b01-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b01-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83b01-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b01-119">입력</span><span class="sxs-lookup"><span data-stu-id="83b01-119">INPUTS</span></span>

### <span data-ttu-id="83b01-120">없음</span><span class="sxs-lookup"><span data-stu-id="83b01-120">None</span></span>

## <span data-ttu-id="83b01-121">출력</span><span class="sxs-lookup"><span data-stu-id="83b01-121">OUTPUTS</span></span>

### <span data-ttu-id="83b01-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83b01-122">System.Boolean</span></span>

## <span data-ttu-id="83b01-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83b01-123">NOTES</span></span>

## <span data-ttu-id="83b01-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83b01-124">RELATED LINKS</span></span>
