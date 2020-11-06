---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530660"
---
# <span data-ttu-id="a98d4-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a98d4-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="a98d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a98d4-103">현재 자격 증명 모음에 대 한 사이트 복구 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a98d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a98d4-104">SYNTAX</span></span>

### <span data-ttu-id="a98d4-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a98d4-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="a98d4-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="a98d4-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="a98d4-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="a98d4-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a98d4-110">설명은</span><span class="sxs-lookup"><span data-stu-id="a98d4-110">DESCRIPTION</span></span>
<span data-ttu-id="a98d4-111">**AzureRmSiteRecoveryNetworkMapping** cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 Azure Site recovery 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="a98d4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a98d4-112">EXAMPLES</span></span>

## <span data-ttu-id="a98d4-113">변수</span><span class="sxs-lookup"><span data-stu-id="a98d4-113">PARAMETERS</span></span>

### <span data-ttu-id="a98d4-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="a98d4-114">-Azure</span></span>
<span data-ttu-id="a98d4-115">명령이 Azure 가상 네트워크에 매핑된 주 서버에 있는 네트워크의 네트워크 매핑 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98d4-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="a98d4-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a98d4-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="a98d4-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a98d4-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="a98d4-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98d4-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="a98d4-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98d4-120">-DefaultProfile</span></span>
<span data-ttu-id="a98d4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a98d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98d4-122">CommonParameters</span></span>
<span data-ttu-id="a98d4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98d4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a98d4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98d4-125">입력</span><span class="sxs-lookup"><span data-stu-id="a98d4-125">INPUTS</span></span>

### <span data-ttu-id="a98d4-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a98d4-126">ASRFabric</span></span>
<span data-ttu-id="a98d4-127">' PrimaryFabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="a98d4-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="a98d4-128">ASRServer</span></span>
<span data-ttu-id="a98d4-129">' PrimaryServer ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="a98d4-130">출력</span><span class="sxs-lookup"><span data-stu-id="a98d4-130">OUTPUTS</span></span>

### <span data-ttu-id="a98d4-131">System.webserver. t e r ' 1 [SiteRecovery Rnetworkmapping]</span><span class="sxs-lookup"><span data-stu-id="a98d4-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="a98d4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a98d4-132">NOTES</span></span>

## <span data-ttu-id="a98d4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a98d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="a98d4-134">새로운 AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a98d4-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="a98d4-135">제거-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a98d4-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
