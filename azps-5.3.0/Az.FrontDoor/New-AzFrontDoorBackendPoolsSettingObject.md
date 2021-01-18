---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493012"
---
# <span data-ttu-id="05316-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="05316-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="05316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05316-102">SYNOPSIS</span></span>
<span data-ttu-id="05316-103">Front Door를 만들기 위한 PSBackendPoolsSetting 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05316-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="05316-104">구문</span><span class="sxs-lookup"><span data-stu-id="05316-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05316-105">설명</span><span class="sxs-lookup"><span data-stu-id="05316-105">DESCRIPTION</span></span>
<span data-ttu-id="05316-106">**New-AzFrontDoorBackendpoolsSettingObject** cmdlet은 Front Door를 만들기 위한 새 PSBackendPoolsSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05316-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="05316-107">예제</span><span class="sxs-lookup"><span data-stu-id="05316-107">EXAMPLES</span></span>

### <span data-ttu-id="05316-108">예제 1: 기본값을 사용하여 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="05316-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="05316-109">예제 2: 사용자 지정 값을 사용하여 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="05316-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="05316-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05316-110">PARAMETERS</span></span>

### <span data-ttu-id="05316-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05316-111">-DefaultProfile</span></span>
<span data-ttu-id="05316-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05316-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05316-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="05316-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="05316-114">모든 백end 풀에 HTTPS 요청에 인증서 이름 확인을 적용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="05316-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="05316-115">HTTPS가 아닌 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05316-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05316-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="05316-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="05316-117">백엔드에 요청을 전달할 때 보내고 받는 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="05316-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="05316-118">시간 제한에 도달하면 요청이 실패하고 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="05316-118">When timeout is reached, the request fails and returns.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05316-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05316-119">CommonParameters</span></span>
<span data-ttu-id="05316-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05316-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05316-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05316-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05316-122">입력</span><span class="sxs-lookup"><span data-stu-id="05316-122">INPUTS</span></span>

### <span data-ttu-id="05316-123">없음</span><span class="sxs-lookup"><span data-stu-id="05316-123">None</span></span>

## <span data-ttu-id="05316-124">출력</span><span class="sxs-lookup"><span data-stu-id="05316-124">OUTPUTS</span></span>

### <span data-ttu-id="05316-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="05316-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="05316-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05316-126">NOTES</span></span>

## <span data-ttu-id="05316-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05316-127">RELATED LINKS</span></span>
