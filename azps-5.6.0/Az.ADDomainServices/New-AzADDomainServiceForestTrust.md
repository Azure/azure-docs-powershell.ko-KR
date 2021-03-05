---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986314"
---
# <span data-ttu-id="8185c-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="8185c-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="8185c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8185c-102">SYNOPSIS</span></span>
<span data-ttu-id="8185c-103">ForestTrust에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8185c-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="8185c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8185c-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="8185c-105">설명</span><span class="sxs-lookup"><span data-stu-id="8185c-105">DESCRIPTION</span></span>
<span data-ttu-id="8185c-106">ForestTrust에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8185c-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="8185c-107">예제</span><span class="sxs-lookup"><span data-stu-id="8185c-107">EXAMPLES</span></span>

### <span data-ttu-id="8185c-108">예제 1: ADDomain용 ServiceForestTrust 만들기</span><span class="sxs-lookup"><span data-stu-id="8185c-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="8185c-109">ADDomain용 ServiceForestTrust 만들기</span><span class="sxs-lookup"><span data-stu-id="8185c-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="8185c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8185c-110">PARAMETERS</span></span>

### <span data-ttu-id="8185c-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8185c-111">-FriendlyName</span></span>
<span data-ttu-id="8185c-112">친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8185c-112">Friendly Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8185c-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="8185c-113">-RemoteDnsIP</span></span>
<span data-ttu-id="8185c-114">원격 Dns ips입니다.</span><span class="sxs-lookup"><span data-stu-id="8185c-114">Remote Dns ips.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8185c-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="8185c-115">-TrustDirection</span></span>
<span data-ttu-id="8185c-116">트러스트 방향.</span><span class="sxs-lookup"><span data-stu-id="8185c-116">Trust Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8185c-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="8185c-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="8185c-118">신뢰할 수 있는 도메인 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="8185c-118">Trusted Domain FQDN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8185c-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="8185c-119">-TrustPassword</span></span>
<span data-ttu-id="8185c-120">암호를 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="8185c-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8185c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8185c-121">CommonParameters</span></span>
<span data-ttu-id="8185c-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8185c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8185c-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8185c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8185c-124">입력</span><span class="sxs-lookup"><span data-stu-id="8185c-124">INPUTS</span></span>

## <span data-ttu-id="8185c-125">출력</span><span class="sxs-lookup"><span data-stu-id="8185c-125">OUTPUTS</span></span>

### <span data-ttu-id="8185c-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="8185c-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="8185c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8185c-127">NOTES</span></span>

<span data-ttu-id="8185c-128">별칭</span><span class="sxs-lookup"><span data-stu-id="8185c-128">ALIASES</span></span>

## <span data-ttu-id="8185c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8185c-129">RELATED LINKS</span></span>

