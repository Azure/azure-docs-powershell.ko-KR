---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526631"
---
# <span data-ttu-id="b0698-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b0698-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="b0698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0698-102">SYNOPSIS</span></span>
<span data-ttu-id="b0698-103">Azure Site Recovery 서비스 공급자 로부터 받은 정보를 새로 고칩니다 (서버 새로 고침).</span><span class="sxs-lookup"><span data-stu-id="b0698-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0698-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0698-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0698-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0698-105">DESCRIPTION</span></span>
<span data-ttu-id="b0698-106">**업데이트 AzureRmRecoveryServicesAsrServicesProvider** Cmdlet은 Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="b0698-107">이 cmdlet을 사용 하 여 복구 서비스 공급자 로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="b0698-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b0698-108">EXAMPLES</span></span>

### <span data-ttu-id="b0698-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0698-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="b0698-110">지정 된 ASR services 공급자에서 정보를 새로 고치는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b0698-111">변수</span><span class="sxs-lookup"><span data-stu-id="b0698-111">PARAMETERS</span></span>

### <span data-ttu-id="b0698-112">-확인</span><span class="sxs-lookup"><span data-stu-id="b0698-112">-Confirm</span></span>
<span data-ttu-id="b0698-113">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0698-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0698-114">-DefaultProfile</span></span>
<span data-ttu-id="b0698-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b0698-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0698-116">-InputObject</span></span>
<span data-ttu-id="b0698-117">정보가 업데이트 되는 서버를 식별 하는 ASR services 공급자 개체를 지정 합니다 (새로 고침 됨).</span><span class="sxs-lookup"><span data-stu-id="b0698-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="b0698-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0698-118">-WhatIf</span></span>
<span data-ttu-id="b0698-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0698-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0698-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0698-121">CommonParameters</span></span>
<span data-ttu-id="b0698-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0698-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0698-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0698-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0698-124">입력</span><span class="sxs-lookup"><span data-stu-id="b0698-124">INPUTS</span></span>

### <span data-ttu-id="b0698-125">SiteRecovery. r m/RecoveryServices 공급자</span><span class="sxs-lookup"><span data-stu-id="b0698-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="b0698-126">출력</span><span class="sxs-lookup"><span data-stu-id="b0698-126">OUTPUTS</span></span>

### <span data-ttu-id="b0698-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="b0698-127">System.Object</span></span>

## <span data-ttu-id="b0698-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b0698-128">NOTES</span></span>

## <span data-ttu-id="b0698-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0698-129">RELATED LINKS</span></span>

[<span data-ttu-id="b0698-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b0698-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="b0698-131">제거-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b0698-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
