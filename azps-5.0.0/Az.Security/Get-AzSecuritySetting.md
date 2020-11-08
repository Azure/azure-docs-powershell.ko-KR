---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215877"
---
# <span data-ttu-id="b780b-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="b780b-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="b780b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b780b-102">SYNOPSIS</span></span>
<span data-ttu-id="b780b-103">Azure 보안 센터에서 보안 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="b780b-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="b780b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b780b-104">SYNTAX</span></span>

### <span data-ttu-id="b780b-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b780b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b780b-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="b780b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b780b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b780b-107">DESCRIPTION</span></span>
<span data-ttu-id="b780b-108">Azure 보안 센터에서 Get-AzSecuritySetting cmdlet의 보안 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="b780b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b780b-109">EXAMPLES</span></span>

### <span data-ttu-id="b780b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b780b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="b780b-111">MCAS 데이터 내보내기 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="b780b-112">변수</span><span class="sxs-lookup"><span data-stu-id="b780b-112">PARAMETERS</span></span>

### <span data-ttu-id="b780b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b780b-113">-DefaultProfile</span></span>
<span data-ttu-id="b780b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b780b-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="b780b-115">-SettingName</span></span>
<span data-ttu-id="b780b-116">설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-116">Setting name.</span></span> <span data-ttu-id="b780b-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="b780b-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b780b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b780b-118">CommonParameters</span></span>
<span data-ttu-id="b780b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b780b-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b780b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b780b-121">입력</span><span class="sxs-lookup"><span data-stu-id="b780b-121">INPUTS</span></span>

### <span data-ttu-id="b780b-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b780b-122">System.String</span></span>

## <span data-ttu-id="b780b-123">출력</span><span class="sxs-lookup"><span data-stu-id="b780b-123">OUTPUTS</span></span>

### <span data-ttu-id="b780b-124">Microsoft. i. i m/. 설정. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="b780b-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="b780b-125">Microsoft. PSSecurityDataExportSetting으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b780b-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="b780b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b780b-126">NOTES</span></span>

## <span data-ttu-id="b780b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b780b-127">RELATED LINKS</span></span>
