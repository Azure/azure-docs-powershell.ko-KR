---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529107"
---
# <span data-ttu-id="30e56-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="30e56-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="30e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e56-102">SYNOPSIS</span></span>
<span data-ttu-id="30e56-103">장애 조치 (failover) 작업을 수행 하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30e56-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30e56-105">DESCRIPTION</span></span>
<span data-ttu-id="30e56-106">**AzureRmSiteRecoveryApplyRecoveryPoint** 는 장애 조치 (failover) 작업을 수행 하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="30e56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30e56-107">EXAMPLES</span></span>

## <span data-ttu-id="30e56-108">변수</span><span class="sxs-lookup"><span data-stu-id="30e56-108">PARAMETERS</span></span>

### <span data-ttu-id="30e56-109">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="30e56-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="30e56-110">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="30e56-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="30e56-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="30e56-111">-RecoveryPoint</span></span>
<span data-ttu-id="30e56-112">이 cmdlet이 변경 하는 복구 시점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e56-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30e56-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="30e56-114">복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30e56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e56-115">-DefaultProfile</span></span>
<span data-ttu-id="30e56-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e56-117">CommonParameters</span></span>
<span data-ttu-id="30e56-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e56-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e56-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e56-120">입력</span><span class="sxs-lookup"><span data-stu-id="30e56-120">INPUTS</span></span>

### <span data-ttu-id="30e56-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30e56-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="30e56-122">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e56-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="30e56-123">출력</span><span class="sxs-lookup"><span data-stu-id="30e56-123">OUTPUTS</span></span>

### <span data-ttu-id="30e56-124">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="30e56-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30e56-125">상속자</span><span class="sxs-lookup"><span data-stu-id="30e56-125">NOTES</span></span>

## <span data-ttu-id="30e56-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30e56-126">RELATED LINKS</span></span>

[<span data-ttu-id="30e56-127">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30e56-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
