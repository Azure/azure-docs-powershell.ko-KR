---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703733"
---
# <span data-ttu-id="12ee3-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="12ee3-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="12ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="12ee3-103">기록 된 범주와 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ee3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12ee3-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12ee3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="12ee3-106">**AzureRmDiagnosticSetting** cmdlet은 리소스에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="12ee3-107">시간 세분화는 메트릭의 집계 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="12ee3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="12ee3-108">EXAMPLES</span></span>

### <span data-ttu-id="12ee3-109">예제 1: 로깅 범주 및 시간 grains의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="12ee3-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="12ee3-110">이 명령은/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.의 *ResourceId* 로 Azure Key Vault에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="12ee3-111">변수</span><span class="sxs-lookup"><span data-stu-id="12ee3-111">PARAMETERS</span></span>

### <span data-ttu-id="12ee3-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ee3-112">-ResourceId</span></span>
<span data-ttu-id="12ee3-113">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-113">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ee3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ee3-114">-DefaultProfile</span></span>
<span data-ttu-id="12ee3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ee3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ee3-116">CommonParameters</span></span>
<span data-ttu-id="12ee3-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ee3-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ee3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ee3-119">입력</span><span class="sxs-lookup"><span data-stu-id="12ee3-119">INPUTS</span></span>

## <span data-ttu-id="12ee3-120">출력</span><span class="sxs-lookup"><span data-stu-id="12ee3-120">OUTPUTS</span></span>

### <span data-ttu-id="12ee3-121">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ee3-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="12ee3-122">상속자</span><span class="sxs-lookup"><span data-stu-id="12ee3-122">NOTES</span></span>

## <span data-ttu-id="12ee3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12ee3-123">RELATED LINKS</span></span>

[<span data-ttu-id="12ee3-124">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="12ee3-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


