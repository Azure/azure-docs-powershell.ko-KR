---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971088"
---
# <span data-ttu-id="441af-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="441af-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="441af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441af-102">SYNOPSIS</span></span>
<span data-ttu-id="441af-103">Front Door 만들기를 위한 PSBackendPoolsSetting 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="441af-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="441af-104">구문</span><span class="sxs-lookup"><span data-stu-id="441af-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="441af-105">설명</span><span class="sxs-lookup"><span data-stu-id="441af-105">DESCRIPTION</span></span>
<span data-ttu-id="441af-106">**New-AzFrontDoorBackendpoolsSettingObject** cmdlet은 Front Door 만들기를 위한 새 PSBackendPoolsSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="441af-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="441af-107">예제</span><span class="sxs-lookup"><span data-stu-id="441af-107">EXAMPLES</span></span>

### <span data-ttu-id="441af-108">예제 1: 기본값을 사용하여 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="441af-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="441af-109">예제 2: 사용자 지정 값으로 BackendPoolsSettings 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="441af-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="441af-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="441af-110">PARAMETERS</span></span>

### <span data-ttu-id="441af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441af-111">-DefaultProfile</span></span>
<span data-ttu-id="441af-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="441af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="441af-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="441af-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="441af-114">모든 백던드 풀에 HTTPS 요청에 대한 인증서 이름 검사를 적용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="441af-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="441af-115">HTTPS가 아닌 요청에는 영향을주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="441af-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="441af-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="441af-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="441af-117">백엔드에 요청을 전달하는 데 대한 시간 제한을 보내고 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="441af-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="441af-118">시간 제한에 도달하면 요청이 실패하고 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="441af-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="441af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441af-119">CommonParameters</span></span>
<span data-ttu-id="441af-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="441af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441af-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="441af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441af-122">입력</span><span class="sxs-lookup"><span data-stu-id="441af-122">INPUTS</span></span>

### <span data-ttu-id="441af-123">없음</span><span class="sxs-lookup"><span data-stu-id="441af-123">None</span></span>

## <span data-ttu-id="441af-124">출력</span><span class="sxs-lookup"><span data-stu-id="441af-124">OUTPUTS</span></span>

### <span data-ttu-id="441af-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="441af-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="441af-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="441af-126">NOTES</span></span>

## <span data-ttu-id="441af-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="441af-127">RELATED LINKS</span></span>
