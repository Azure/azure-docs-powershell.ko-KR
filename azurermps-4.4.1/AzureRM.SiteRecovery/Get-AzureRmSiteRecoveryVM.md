---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702685"
---
# <span data-ttu-id="a2910-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a2910-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="a2910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2910-102">SYNOPSIS</span></span>
<span data-ttu-id="a2910-103">사이트 복구 관리 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2910-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2910-104">SYNTAX</span></span>

### <span data-ttu-id="a2910-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2910-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2910-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a2910-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2910-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2910-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2910-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a2910-108">DESCRIPTION</span></span>
<span data-ttu-id="a2910-109">**AzureRmSiteRecoveryVM** Cmdlet은 Azure Site Recovery에서 관리 되는 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="a2910-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a2910-110">EXAMPLES</span></span>

## <span data-ttu-id="a2910-111">변수</span><span class="sxs-lookup"><span data-stu-id="a2910-111">PARAMETERS</span></span>

### <span data-ttu-id="a2910-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a2910-112">-FriendlyName</span></span>
<span data-ttu-id="a2910-113">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-113">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2910-114">-이름</span><span class="sxs-lookup"><span data-stu-id="a2910-114">-Name</span></span>
<span data-ttu-id="a2910-115">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2910-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a2910-116">-ProtectionContainer</span></span>
<span data-ttu-id="a2910-117">사이트 복구 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2910-118">-DefaultProfile</span></span>
<span data-ttu-id="a2910-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2910-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2910-120">CommonParameters</span></span>
<span data-ttu-id="a2910-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2910-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2910-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2910-123">입력</span><span class="sxs-lookup"><span data-stu-id="a2910-123">INPUTS</span></span>

### <span data-ttu-id="a2910-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a2910-124">ASRProtectionContainer</span></span>
<span data-ttu-id="a2910-125">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="a2910-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a2910-126">ASRProtectionContainer</span></span>
<span data-ttu-id="a2910-127">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2910-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="a2910-128">출력</span><span class="sxs-lookup"><span data-stu-id="a2910-128">OUTPUTS</span></span>

### <span data-ttu-id="a2910-129">System.webserver. t e 1.aspx ' 1 [Microsoft SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="a2910-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="a2910-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a2910-130">NOTES</span></span>

## <span data-ttu-id="a2910-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2910-131">RELATED LINKS</span></span>

[<span data-ttu-id="a2910-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a2910-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
