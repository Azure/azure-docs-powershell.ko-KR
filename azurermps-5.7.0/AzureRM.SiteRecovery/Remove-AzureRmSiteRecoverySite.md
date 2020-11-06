---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: a83b4b8ca3dbe415013fe9a858d46cb886ce4b00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524915"
---
# <span data-ttu-id="b3bac-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b3bac-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="b3bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3bac-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bac-103">현재 자격 증명 모음에서 사이트 복구 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3bac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3bac-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3bac-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bac-106">**AzureRmSiteRecoverySite** cmdlet은 현재 자격 증명 모음에서 Azure Site Recovery 사이트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="b3bac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3bac-107">EXAMPLES</span></span>

## <span data-ttu-id="b3bac-108">변수</span><span class="sxs-lookup"><span data-stu-id="b3bac-108">PARAMETERS</span></span>

### <span data-ttu-id="b3bac-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bac-109">-DefaultProfile</span></span>
<span data-ttu-id="b3bac-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3bac-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b3bac-111">-Force</span></span>
<span data-ttu-id="b3bac-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bac-113">-사이트</span><span class="sxs-lookup"><span data-stu-id="b3bac-113">-Site</span></span>
<span data-ttu-id="b3bac-114">사이트 복구 사이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-114">Specifies the Site Recovery site object.</span></span>

```yaml
Type: ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3bac-115">-확인</span><span class="sxs-lookup"><span data-stu-id="b3bac-115">-Confirm</span></span>
<span data-ttu-id="b3bac-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bac-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bac-117">-WhatIf</span></span>
<span data-ttu-id="b3bac-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b3bac-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3bac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bac-120">CommonParameters</span></span>
<span data-ttu-id="b3bac-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bac-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3bac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bac-123">입력</span><span class="sxs-lookup"><span data-stu-id="b3bac-123">INPUTS</span></span>

### <span data-ttu-id="b3bac-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="b3bac-124">ASRSite</span></span>
<span data-ttu-id="b3bac-125">' Site ' 매개 변수는 파이프라인에서 ' ASRSite ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3bac-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="b3bac-126">출력</span><span class="sxs-lookup"><span data-stu-id="b3bac-126">OUTPUTS</span></span>

## <span data-ttu-id="b3bac-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b3bac-127">NOTES</span></span>

## <span data-ttu-id="b3bac-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3bac-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3bac-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b3bac-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="b3bac-130">새로운 AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="b3bac-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
