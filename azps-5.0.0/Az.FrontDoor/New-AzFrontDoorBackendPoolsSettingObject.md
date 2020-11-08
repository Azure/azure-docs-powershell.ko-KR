---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217423"
---
# <span data-ttu-id="18bc0-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="18bc0-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="18bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="18bc0-103">전방 도어 만들기에 대 한 PSBackendPoolsSetting 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="18bc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18bc0-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bc0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="18bc0-106">**AzFrontDoorBackendpoolsSettingObject** Cmdlet은 전방 문을 만들기 위해 새로운 PSBackendPoolsSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="18bc0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="18bc0-107">EXAMPLES</span></span>

### <span data-ttu-id="18bc0-108">예제 1: 기본값을 사용 하 여 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="18bc0-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="18bc0-109">예제 2: 사용자가 지정한 값을 사용 하 여 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="18bc0-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="18bc0-110">변수</span><span class="sxs-lookup"><span data-stu-id="18bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="18bc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bc0-111">-DefaultProfile</span></span>
<span data-ttu-id="18bc0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18bc0-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="18bc0-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="18bc0-114">모든 백 엔드 풀에 대 한 HTTPS 요청에서 인증서 이름을 적용할지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="18bc0-115">비 HTTPS 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="18bc0-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="18bc0-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="18bc0-117">요청을 백 엔드로 전달 하는 동안 보내기 및 받기 시간 제한.</span><span class="sxs-lookup"><span data-stu-id="18bc0-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="18bc0-118">제한 시간에 도달 하면 요청이 실패 하 고 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="18bc0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bc0-119">CommonParameters</span></span>
<span data-ttu-id="18bc0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18bc0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bc0-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18bc0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bc0-122">입력</span><span class="sxs-lookup"><span data-stu-id="18bc0-122">INPUTS</span></span>

### <span data-ttu-id="18bc0-123">않아야</span><span class="sxs-lookup"><span data-stu-id="18bc0-123">None</span></span>

## <span data-ttu-id="18bc0-124">출력</span><span class="sxs-lookup"><span data-stu-id="18bc0-124">OUTPUTS</span></span>

### <span data-ttu-id="18bc0-125">FrontDoor. PSBackendPoolsSetting/.</span><span class="sxs-lookup"><span data-stu-id="18bc0-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="18bc0-126">상속자</span><span class="sxs-lookup"><span data-stu-id="18bc0-126">NOTES</span></span>

## <span data-ttu-id="18bc0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18bc0-127">RELATED LINKS</span></span>
