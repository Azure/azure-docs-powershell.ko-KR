---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529118"
---
# <span data-ttu-id="5b8b9-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5b8b9-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="5b8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8b9-103">현재 자격 증명 모음의 사이트 복구에서 관리 되는 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b8b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b8b9-104">SYNTAX</span></span>

### <span data-ttu-id="5b8b9-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5b8b9-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="5b8b9-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="5b8b9-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="5b8b9-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="5b8b9-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-110">ByName</span><span class="sxs-lookup"><span data-stu-id="5b8b9-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b8b9-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5b8b9-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b8b9-112">설명은</span><span class="sxs-lookup"><span data-stu-id="5b8b9-112">DESCRIPTION</span></span>
<span data-ttu-id="5b8b9-113">**AzureRmSiteRecoveryNetwork** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5b8b9-114">예제의</span><span class="sxs-lookup"><span data-stu-id="5b8b9-114">EXAMPLES</span></span>

## <span data-ttu-id="5b8b9-115">변수</span><span class="sxs-lookup"><span data-stu-id="5b8b9-115">PARAMETERS</span></span>

### <span data-ttu-id="5b8b9-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="5b8b9-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8b9-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5b8b9-117">-FriendlyName</span></span>
<span data-ttu-id="5b8b9-118">가상 컴퓨터 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8b9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5b8b9-119">-Name</span></span>
<span data-ttu-id="5b8b9-120">가상 컴퓨터 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8b9-121">-서버</span><span class="sxs-lookup"><span data-stu-id="5b8b9-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8b9-122">-DefaultProfile</span></span>
<span data-ttu-id="5b8b9-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b8b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8b9-124">CommonParameters</span></span>
<span data-ttu-id="5b8b9-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8b9-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8b9-127">입력</span><span class="sxs-lookup"><span data-stu-id="5b8b9-127">INPUTS</span></span>

### <span data-ttu-id="5b8b9-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5b8b9-128">ASRFabric</span></span>
<span data-ttu-id="5b8b9-129">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="5b8b9-130">이름</span><span class="sxs-lookup"><span data-stu-id="5b8b9-130">String</span></span>
<span data-ttu-id="5b8b9-131">' FriendlyName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b8b9-132">이름</span><span class="sxs-lookup"><span data-stu-id="5b8b9-132">String</span></span>
<span data-ttu-id="5b8b9-133">' FriendlyName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b8b9-134">이름</span><span class="sxs-lookup"><span data-stu-id="5b8b9-134">String</span></span>
<span data-ttu-id="5b8b9-135">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b8b9-136">이름</span><span class="sxs-lookup"><span data-stu-id="5b8b9-136">String</span></span>
<span data-ttu-id="5b8b9-137">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b8b9-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="5b8b9-138">ASRServer</span></span>
<span data-ttu-id="5b8b9-139">' Server ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="5b8b9-140">출력</span><span class="sxs-lookup"><span data-stu-id="5b8b9-140">OUTPUTS</span></span>

### <span data-ttu-id="5b8b9-141">System.webserver. t e r ' 1 [SiteRecovery],,.</span><span class="sxs-lookup"><span data-stu-id="5b8b9-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="5b8b9-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5b8b9-142">NOTES</span></span>

## <span data-ttu-id="5b8b9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b8b9-143">RELATED LINKS</span></span>

