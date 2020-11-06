---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534579"
---
# <span data-ttu-id="1b649-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1b649-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="1b649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b649-102">SYNOPSIS</span></span>
<span data-ttu-id="1b649-103">장애 조치 (failover) 작업을 수행 하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b649-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b649-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b649-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1b649-105">DESCRIPTION</span></span>
<span data-ttu-id="1b649-106">**AzureRmSiteRecoveryApplyRecoveryPoint** 는 장애 조치 (failover) 작업을 수행 하기 전에 실패 한 보호 항목을 통해 복구 지점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="1b649-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1b649-107">EXAMPLES</span></span>

## <span data-ttu-id="1b649-108">변수</span><span class="sxs-lookup"><span data-stu-id="1b649-108">PARAMETERS</span></span>

### <span data-ttu-id="1b649-109">-Data Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="1b649-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b649-110">-Data Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="1b649-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b649-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b649-111">-DefaultProfile</span></span>
<span data-ttu-id="1b649-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b649-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1b649-113">-RecoveryPoint</span></span>
<span data-ttu-id="1b649-114">이 cmdlet이 변경 하는 복구 시점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-114">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b649-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b649-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1b649-116">복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-116">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b649-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b649-117">CommonParameters</span></span>
<span data-ttu-id="1b649-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b649-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b649-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b649-120">입력</span><span class="sxs-lookup"><span data-stu-id="1b649-120">INPUTS</span></span>

### <span data-ttu-id="1b649-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b649-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1b649-122">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b649-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1b649-123">출력</span><span class="sxs-lookup"><span data-stu-id="1b649-123">OUTPUTS</span></span>

### <span data-ttu-id="1b649-124">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="1b649-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1b649-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1b649-125">NOTES</span></span>

## <span data-ttu-id="1b649-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b649-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b649-127">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b649-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
