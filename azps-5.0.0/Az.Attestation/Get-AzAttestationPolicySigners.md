---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicysigners
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
ms.openlocfilehash: f9635a4958d0daefdba075340f66af832bd2b168
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307604"
---
# <span data-ttu-id="11ec7-101">Get-AzAttestationPolicySigners</span><span class="sxs-lookup"><span data-stu-id="11ec7-101">Get-AzAttestationPolicySigners</span></span>

## <span data-ttu-id="11ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="11ec7-103">Azure 증명의 테 넌 트에서 신뢰할 수 있는 정책 서명자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-103">Gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="11ec7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11ec7-104">SYNTAX</span></span>

### <span data-ttu-id="11ec7-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11ec7-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ec7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11ec7-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11ec7-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="11ec7-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-Location] <String> [-DefaultProvider]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11ec7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="11ec7-108">DESCRIPTION</span></span>
<span data-ttu-id="11ec7-109">Get-AzAttestationPolicySigners cmdlet은 Azure 증명의 테 넌 트에서 신뢰할 수 있는 정책 서명자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-109">The Get-AzAttestationPolicySigners cmdlet gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="11ec7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="11ec7-110">EXAMPLES</span></span>

### <span data-ttu-id="11ec7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="11ec7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                          
CertificateCount : 0
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdC51cy5hdHRlc3QuYXp1cmUubmV0L2NlcnRzIiwgImtpZCI6ICJrdlB4aUJlemk4RGJsQVY0WE5nNG5wVjlocE5WTnRqS0NQTlZZUjRuRVJzPSIsICJ0eXAiOiAiSldUIn0.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW119LCAiZXhwIjogMTU4NDM5NDgxOSwgImlhdCI6IDE1ODQzOTEyMTksICJpc3MiOiAiaHR0cHM6Ly9wc2h0ZXN0LnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTIxOX0.hXDejUE2Tfbnvy0RN4ONyxtg2NTEmHKz7wOJIY2YhF43MUJQYgh7TREE3BAMl93mQIO9px2HNvo_MSzNhDRmCMvZt6tUdC8Gw1xK40w2nqngvfmTONOcKskSXUVc1Igk2C47cuCQjB1W8t2qdCrwpR4UTEGdidyGlb7NFkAaFMOK119H1c0DQ7LSpY0bqodrVDW1DNa0LOFLxL3DwxqkRF-itk
duZJn9aqlkrgIPPSE_kdNUUURjpx3F6eCEONsdtu8zfj76v7Yb6Oyf70rh8EOyVdEu2wwmfg9ASZnooANwo7C6o68ESpfvi6DHPTyBsD0rgysVsNYtkS0tuXNj3A
Algorithm        : RS256
JKU              : https://pshtest.us.attest.azure.net/certs
Certificates     : {}
```

<span data-ttu-id="11ec7-112">리소스 그룹 *psh-rg* 의 증명 공급자 *pshtest* 에 대 한 신뢰할 수 있는 정책 서명자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-112">Gets the trusted policy signers for the Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="11ec7-113">이 증명 공급자에 대 한 신뢰할 수 있는 서명자가 없는 것을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="11ec7-113">Note that there are no trusted signers for this Attestation Provider.</span></span>

### <span data-ttu-id="11ec7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="11ec7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest2 -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                         
CertificateCount : 1
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdDIudXMuYXR0ZXN0LmF6dXJlLm5ldC9jZXJ0cyIsICJraWQiOiAiL09KMXJ0U0hkbFJnR1VqMGVuTEl5bDhLeHQ3NHZYdmJLTW9VbmFZMlNJRT0iLCAidHlwIjogIkpXVCJ9.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW3siYWxnIjogIlJTMjU2IiwgImt0eSI6ICJSU0EiLCAidXNlIjogInNpZyIsICJ4NWMiOiBbIk1JSURMRENDQWhTZ0F3SUJBZ0lJYStGTE1oT1ZkMFF3RFFZSktvWklodmNOQVFFTEJRQXdGekVWTUJNR0ExVUVBd3dNVFdGaFZHVnpkRU5sY25ReE1DQVhEVEl3TURNd016QXdNREF3TUZvWUR6SXdOekF3TXpBek1EQXdNREF3V2pBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREV3Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLQW9JQkFRQ3BidzRLeHJhME05OE9RNUMzQkk3Uk9BS2k4dnlRNTF5eWJoUi9saTJDd1Y4WkVJZmVZSEJMMFM5UC9naVQ2VTlZRkNtNEw3c2hGTm5kYTBJcG5zeTZSaFhCUnRYampZdVR1SlcxTk01SVh0OVFJMEtkUUNQbG5VVlNnb2UzdW9pQ0l6S25HU1Nka0MrU25nblVveDFsVnVRNEpLSmtLUXBubTFCekgzTGNzUEFnQUJwYTloVnlieG9XUHU4c2tEek1TSVFZVzMxemVYVkxZdlprZmxoTWttNFZLby9DUWpYNXJWTFNXeVZWa1YrOUhDQjlVQk1HMExiNmhldWZTQTVKTE5mR2taY0kwNHBHRmFqVzZnVUJkcmJnM2R4V0s5VzdKUVZYT05maEJ6NkE2bWM1a0wxRUtLNWhIc2dnekdYeEdLWmhwWU5JSDNiek52eTNrUUFQQWdNQkFBR2plakI0TUVZR0ExVWRJd1EvTUQyQUZIWnBTaFI4UUlRMGFzZy9Yb1NwR2hNOURGN25vUnVrR1RBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREdDQ0d2aFN6SVRsWGRFTUIwR0ExVWREZ1FXQkJSMmFVb1VmRUNFTkdySVAxNkVxUm9UUFF4ZTV6QVBCZ05WSFJNQkFmOEVCVEFEQVFIL01BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRQVFpWXpFeUtVbDlkSWVUVGZnTVpBWEo0V0NFZXpFN2FRcHd2QnU5Rkk0MXN4L1pzbEV2RVFvTDVWNTZTQVhQZCtTOWdlZnVJNjFuZ056OTl5RTlrZGgrOWxmVTJVTU1tdXFCdVFWaWI5RzBKakllYVNHM1J2OGVyRXNGMUUrbXhjbzRtVGVEdUdLUklmN1dHNnNYZjZ5b2N1U0FVaEV2emM5NzZTSUNJLzQxclZEVkg5bnFJdS9LUnZleHpWcFJqZ1EzWlVnMTMydmVnb2djNjc1UndreTJHckxrZDBJN015bGcwZVIyamd1ZndLcTVBbnZ1YTlzRFJyUUpLUCtqclpmcWpiOEpoZ2VsUEtLVXl4S1JIS1Z6QUxzQ3JHTkRQS0ozVDlsWUhmZmFuWE9JeEpnTDExcDNBMmVMUWtWN3BMdEpUenhrb1lDZFZKdTNmbDZJNWVsIl19XX0sICJleHAiOiAxNTg0Mzk1MTE5LCAiaWF0IjogMTU4NDM5MTUxOSwgImlzcyI6ICJodHRwczovL3BzaHRlc3QyLnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTUxOX0Irkd3eNG7jD-fJThxBKURjjSlsfbRgOnOvN_nI8ukH-VvpaYIKGgk74iuefWhPYQJr--mAUT2IaEqcBGXvRV6K4oDUXUHn7iCNL1aIWzQ4udTrFVChNTUjEH4x1tmyDLC04SBeoi_yP5R0Bfijb51qnKwSU6ppuKTTletpzFztib2MN_RUQidHjuaeivMECJPRu5Bit2DbLRObokMRRY-rftcxPf7rLr1mK_4WUbRjIKT_ic03qWcqY0lakwC3MdFV9xQsvCH7-sizgJShSIOIS9pHrRp6YIEyG8LoF6Kj9aL-imNTUZ2IjwxtDJOmnhXh56pYjzQNpW_bzQlOeNaA
Algorithm        : RS256
JKU              : https://pshtest2.us.attest.azure.net/certs
Certificates     : {{
                     "alg": "RS256",
                     "kty": "RSA",
                     "use": "sig",
                     "x5c": ["MIIDLDCCAhSgAwIBAgIIa+FLMhOVd0QwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAwwMTWFhVGVzdENlcnQxMCAXDTIwMDMwMzAwMDAwMFoYDzIwNzAwMzAzMDAwMDAwWjAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDEwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCpbw4Kxra0M98OQ5C3BI7ROAKi8vyQ51yybhR/li2CwV8ZEIfeYHBL0S9P/giT6U9YFCm4L7shFNnda0Ipnsy6RhXBRtXjjYuTuJW1NM5IXt9QI0KdQCPlnUVSgoe3uoiCIzKnGSSdkC+SngnUox1lVuQ4JKJkKQpnm1BzH3LcsPAgABpa9hVybxoWPu8skDzMSIQYW31zeXVLYvZkflhMkm4VKo/CQjX5rVLSWyVVkV+9HCB9UBMG0Lb6heufSA5JLNfGkZcI04pGFajW6gUBdrbg3dxWK9W7JQVXONfhBz6A6mc5kL1EKK5hHsggzGXxGKZhpYNIH3bzNvy3kQAPAgMBAAGjejB4MEYGA1UdIwQ/MD2AFHZpShR8QIQ0asg/XoSpGhM9DF7noRukGTAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDGCCGvhSzITlXdEMB0GA1UdDgQWBBR2aUoUfECENGrIP16EqRoTPQxe5zAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQAQiYzEyKUl9dIeTTfgMZAXJ4WCEezE7aQpwvBu9FI41sx/ZslEvEQoL5V56SAXPd+S9gefuI61ngNz99yE9kdh+9lfU2UMMmuqBuQVib9G0JjIeaSG3Rv8erEsF1E+mxco4mTeDuGKRIf7WG6sXf6yocuSAUhEvzc976SICI/41rVDVH9nqIu/KRvexzVpRjgQ3ZUg132vegogc675Rwky2GrLkd0I7Mylg0eR2jgufwKq5Anvua9sDRrQJKP+jrZfqjb8JhgelPKKUyxKRHKVzALsCrGNDPKJ3T9lYHffanXOIxJgL11p3A2eLQkV7pLtJTzxkoYCdVJu3fl6I5el"]
                   }}
```

<span data-ttu-id="11ec7-115">리소스 그룹 *psh-rg* 의 증명 공급자 *pshtest2* 에 대 한 신뢰할 수 있는 정책 서명자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-115">Gets the trusted policy signers for the Attestation Provider *pshtest2* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="11ec7-116">이 증명 공급자에 대 한 신뢰할 수 있는 서명자가 하나 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="11ec7-116">Note that there is one trusted signer for this Attestation Provider.</span></span>

### <span data-ttu-id="11ec7-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="11ec7-117">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -DefaultProvider -Location "Central US"
CertificateCount : 0
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vc2hhcmVkZXVzLmV1cy50ZXN0LmF0dGVzdC5henVyZS5uZXQvY2VydHMi
                   LCAia2lkIjogIlhodGZtZlR0bS9MNnhUUkU2RGoxc3BTVkpSRnAwcXdyTjNRem9RWHJwR0E9IiwgInR5cCI6ICJKV1QifQ.eyJhY
                   XMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW119LCAiZXhwIjogMTU5Mzc1ODEyOCwgImlhdCI6IDE1OTM3NTQ1MjgsI
                   CJpc3MiOiAiaHR0cHM6Ly9zaGFyZWRldXMuZXVzLnRlc3QuYXR0ZXN0LmF6dXJlLm5ldCIsICJtYWEtcG9saWN5Q2VydGlmaWNhd
                   GVzIjogeyJrZXlzIjogW119LCAibmJmIjogMTU5Mzc1NDUyOH0.C1FPzJVuAQQszL1s-5FpiZf4YDF7VD6cYnoy0S9QFAQYlJOy-
                   PX00GT_uCnOHKzPvhwQ-doiQCkEhIRpA6coK9gEU4k_R4KK5kmtWZEpzDGo2M-8ScIsVQlN0-nITfMk4kf4nRZgiqWSr_X7nuWCD
                   7Ddhj0OrKWK_6Cz6WlktGrjdhozU0-HNNTy6DKWcLB3cubPY9j6L9Uyvu4uO5m1QjN_Cn4G_6Zq21aM89kOcUzDgpHYralrNXkKH
                   3XBRKfGcQqatJky8Tq3s5Kd-0TRokOsekH681fMTFv_K2R6ORxOPoh7h-dX7LysmSGqmX_7GqhAgTGGXBaGekO6BNRe1A
Algorithm        : RS256
JKU              : https://sharedcus.cus.attest.azure.net/certs
Certificates     : {}
```

<span data-ttu-id="11ec7-118">*중앙 US* 의 증명 기본 공급자에 대 한 신뢰할 수 있는 정책 서명자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-118">Gets the trusted policy signers for the Attestation Default Provider in Location *Central US*.</span></span>  <span data-ttu-id="11ec7-119">증명 기본 공급자에 대 한 신뢰할 수 있는 서명자가 없는 것을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="11ec7-119">Note that there are no trusted signers for Attestation Default Provider.</span></span>

## <span data-ttu-id="11ec7-120">변수</span><span class="sxs-lookup"><span data-stu-id="11ec7-120">PARAMETERS</span></span>

### <span data-ttu-id="11ec7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ec7-121">-DefaultProfile</span></span>
<span data-ttu-id="11ec7-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ec7-123">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="11ec7-123">-DefaultProvider</span></span>
<span data-ttu-id="11ec7-124">기본 증명 공급자에 대 한 요청 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-124">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ec7-125">-위치</span><span class="sxs-lookup"><span data-stu-id="11ec7-125">-Location</span></span>
<span data-ttu-id="11ec7-126">기본 증명 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-126">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ec7-127">-이름</span><span class="sxs-lookup"><span data-stu-id="11ec7-127">-Name</span></span>
<span data-ttu-id="11ec7-128">증명 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-128">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ec7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ec7-129">-ResourceGroupName</span></span>
<span data-ttu-id="11ec7-130">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-130">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ec7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ec7-131">-ResourceId</span></span>
<span data-ttu-id="11ec7-132">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-132">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ec7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ec7-133">CommonParameters</span></span>
<span data-ttu-id="11ec7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ec7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ec7-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11ec7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ec7-136">입력</span><span class="sxs-lookup"><span data-stu-id="11ec7-136">INPUTS</span></span>

### <span data-ttu-id="11ec7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11ec7-137">System.String</span></span>

## <span data-ttu-id="11ec7-138">출력</span><span class="sxs-lookup"><span data-stu-id="11ec7-138">OUTPUTS</span></span>

### <span data-ttu-id="11ec7-139">PSPolicySigners/. i m m</span><span class="sxs-lookup"><span data-stu-id="11ec7-139">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="11ec7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="11ec7-140">NOTES</span></span>

## <span data-ttu-id="11ec7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11ec7-141">RELATED LINKS</span></span>
