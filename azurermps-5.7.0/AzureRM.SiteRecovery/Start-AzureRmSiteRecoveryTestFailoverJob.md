---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526563"
---
# <span data-ttu-id="64c96-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="64c96-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="64c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c96-102">SYNOPSIS</span></span>
<span data-ttu-id="64c96-103">사이트 복구 보호 엔터티에 대 한 테스트 장애 조치를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64c96-104">SYNTAX</span></span>

### <span data-ttu-id="64c96-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="64c96-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="64c96-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="64c96-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="64c96-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="64c96-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="64c96-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="64c96-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="64c96-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c96-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="64c96-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64c96-114">설명은</span><span class="sxs-lookup"><span data-stu-id="64c96-114">DESCRIPTION</span></span>
<span data-ttu-id="64c96-115">**AzureRmSiteRecoveryTestFailoverJob** Cmdlet은 Azure Site Recovery 보호 엔터티 또는 복구 계획의 장애 조치 테스트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="64c96-116">Get-AzureRmSiteRecoveryJob cmdlet을 사용 하 여 작업 성공 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="64c96-117">예제의</span><span class="sxs-lookup"><span data-stu-id="64c96-117">EXAMPLES</span></span>

## <span data-ttu-id="64c96-118">변수</span><span class="sxs-lookup"><span data-stu-id="64c96-118">PARAMETERS</span></span>

### <span data-ttu-id="64c96-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="64c96-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="64c96-120">Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-121">-Data<c13> Primarycertfile</span><span class="sxs-lookup"><span data-stu-id="64c96-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="64c96-122">기본 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="64c96-123">-Data<c13> Secondarycertfile</span><span class="sxs-lookup"><span data-stu-id="64c96-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="64c96-124">보조 인증서 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="64c96-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c96-125">-DefaultProfile</span></span>
<span data-ttu-id="64c96-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64c96-127">방향</span><span class="sxs-lookup"><span data-stu-id="64c96-127">-Direction</span></span>
<span data-ttu-id="64c96-128">장애 조치 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-128">Specifies the failover direction.</span></span>
<span data-ttu-id="64c96-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64c96-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="64c96-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="64c96-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="64c96-131">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="64c96-132">-ProtectionEntity</span></span>
<span data-ttu-id="64c96-133">사이트 복구 보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64c96-134">-RecoveryPlan</span></span>
<span data-ttu-id="64c96-135">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64c96-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="64c96-137">-VMNetwork</span></span>
<span data-ttu-id="64c96-138">사이트 복구 가상 컴퓨터 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c96-139">CommonParameters</span></span>
<span data-ttu-id="64c96-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c96-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c96-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c96-142">입력</span><span class="sxs-lookup"><span data-stu-id="64c96-142">INPUTS</span></span>

### <span data-ttu-id="64c96-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="64c96-143">ASRProtectionEntity</span></span>
<span data-ttu-id="64c96-144">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="64c96-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64c96-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="64c96-146">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="64c96-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64c96-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="64c96-148">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c96-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="64c96-149">출력</span><span class="sxs-lookup"><span data-stu-id="64c96-149">OUTPUTS</span></span>

### <span data-ttu-id="64c96-150">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="64c96-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64c96-151">상속자</span><span class="sxs-lookup"><span data-stu-id="64c96-151">NOTES</span></span>

## <span data-ttu-id="64c96-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64c96-152">RELATED LINKS</span></span>

[<span data-ttu-id="64c96-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="64c96-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
