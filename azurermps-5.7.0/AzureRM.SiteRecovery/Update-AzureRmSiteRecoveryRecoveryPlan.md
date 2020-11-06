---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524884"
---
# <span data-ttu-id="6ba86-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="6ba86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba86-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba86-103">사이트 복구에서 복구 계획을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ba86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ba86-104">SYNTAX</span></span>

### <span data-ttu-id="6ba86-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ba86-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ba86-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6ba86-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ba86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6ba86-107">DESCRIPTION</span></span>
<span data-ttu-id="6ba86-108">**업데이트 AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery의 복구 계획을 업데이트 한 다음 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="6ba86-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6ba86-109">EXAMPLES</span></span>

### <span data-ttu-id="6ba86-110">예제 1: 복구 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="6ba86-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="6ba86-111">이 명령은 지정 된 복구 계획을 업데이트 한 다음 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="6ba86-112">변수</span><span class="sxs-lookup"><span data-stu-id="6ba86-112">PARAMETERS</span></span>

### <span data-ttu-id="6ba86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba86-113">-DefaultProfile</span></span>
<span data-ttu-id="6ba86-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ba86-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6ba86-115">-Path</span></span>
<span data-ttu-id="6ba86-116">이 cmdlet이 업데이트 하는 복구 계획의 복구 계획 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba86-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-117">-RecoveryPlan</span></span>
<span data-ttu-id="6ba86-118">이 cmdlet이 업데이트 하는 복구 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba86-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba86-119">CommonParameters</span></span>
<span data-ttu-id="6ba86-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba86-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba86-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba86-122">입력</span><span class="sxs-lookup"><span data-stu-id="6ba86-122">INPUTS</span></span>

### <span data-ttu-id="6ba86-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="6ba86-124">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba86-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="6ba86-125">출력</span><span class="sxs-lookup"><span data-stu-id="6ba86-125">OUTPUTS</span></span>

## <span data-ttu-id="6ba86-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6ba86-126">NOTES</span></span>

## <span data-ttu-id="6ba86-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ba86-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ba86-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6ba86-129">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6ba86-130">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ba86-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


