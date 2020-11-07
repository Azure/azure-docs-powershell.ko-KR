---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703644"
---
# <span data-ttu-id="8b794-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b794-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8b794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b794-102">SYNOPSIS</span></span>
<span data-ttu-id="8b794-103">Azure Site Recovery 서비스 공급자 로부터 받은 정보를 새로 고칩니다 (서버 새로 고침).</span><span class="sxs-lookup"><span data-stu-id="8b794-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b794-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b794-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b794-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b794-105">DESCRIPTION</span></span>
<span data-ttu-id="8b794-106">**업데이트 AzureRmRecoveryServicesAsrServicesProvider** Cmdlet은 Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="8b794-107">이 cmdlet을 사용 하 여 복구 서비스 공급자 로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="8b794-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8b794-108">EXAMPLES</span></span>

### <span data-ttu-id="8b794-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b794-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="8b794-110">지정 된 ASR services 공급자에서 정보를 새로 고치는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="8b794-111">변수</span><span class="sxs-lookup"><span data-stu-id="8b794-111">PARAMETERS</span></span>

### <span data-ttu-id="8b794-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b794-112">-InputObject</span></span>
<span data-ttu-id="8b794-113">입력 개체: 정보가 업데이트 되는 서버를 식별 하는 ASR 서비스 공급자 (asr services provider) 개체를 지정 합니다 (새로 고침 됨).</span><span class="sxs-lookup"><span data-stu-id="8b794-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-114">-확인</span><span class="sxs-lookup"><span data-stu-id="8b794-114">-Confirm</span></span>
<span data-ttu-id="8b794-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b794-116">-WhatIf</span></span>
<span data-ttu-id="8b794-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b794-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b794-119">CommonParameters</span></span>
<span data-ttu-id="8b794-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b794-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b794-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b794-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b794-122">입력</span><span class="sxs-lookup"><span data-stu-id="8b794-122">INPUTS</span></span>

### <span data-ttu-id="8b794-123">SiteRecovery. r m/RecoveryServices 공급자</span><span class="sxs-lookup"><span data-stu-id="8b794-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8b794-124">출력</span><span class="sxs-lookup"><span data-stu-id="8b794-124">OUTPUTS</span></span>

### <span data-ttu-id="8b794-125">System. 개체</span><span class="sxs-lookup"><span data-stu-id="8b794-125">System.Object</span></span>

## <span data-ttu-id="8b794-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8b794-126">NOTES</span></span>

## <span data-ttu-id="8b794-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b794-127">RELATED LINKS</span></span>

[<span data-ttu-id="8b794-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b794-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8b794-129">제거-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b794-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
