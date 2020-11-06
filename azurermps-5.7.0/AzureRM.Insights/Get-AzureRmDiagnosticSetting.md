---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525096"
---
# <span data-ttu-id="591a2-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="591a2-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="591a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591a2-102">SYNOPSIS</span></span>
<span data-ttu-id="591a2-103">기록 된 범주와 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="591a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="591a2-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="591a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="591a2-105">DESCRIPTION</span></span>
<span data-ttu-id="591a2-106">**AzureRmDiagnosticSetting** cmdlet은 리소스에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="591a2-107">시간 세분화는 메트릭의 집계 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="591a2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="591a2-108">EXAMPLES</span></span>

### <span data-ttu-id="591a2-109">예제 1: 로깅 범주 및 시간 grains의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="591a2-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="591a2-110">이 명령은/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.의 *ResourceId* 로 Azure Key Vault에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="591a2-111">변수</span><span class="sxs-lookup"><span data-stu-id="591a2-111">PARAMETERS</span></span>

### <span data-ttu-id="591a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591a2-112">-DefaultProfile</span></span>
<span data-ttu-id="591a2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="591a2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591a2-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="591a2-114">-ResourceId</span></span>
<span data-ttu-id="591a2-115">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-115">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591a2-116">CommonParameters</span></span>
<span data-ttu-id="591a2-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591a2-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591a2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591a2-119">입력</span><span class="sxs-lookup"><span data-stu-id="591a2-119">INPUTS</span></span>

### <span data-ttu-id="591a2-120">않아야</span><span class="sxs-lookup"><span data-stu-id="591a2-120">None</span></span>
<span data-ttu-id="591a2-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="591a2-122">출력</span><span class="sxs-lookup"><span data-stu-id="591a2-122">OUTPUTS</span></span>

### <span data-ttu-id="591a2-123">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="591a2-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="591a2-124">상속자</span><span class="sxs-lookup"><span data-stu-id="591a2-124">NOTES</span></span>

## <span data-ttu-id="591a2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="591a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="591a2-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="591a2-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


