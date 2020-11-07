---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 41923067729b50a77f8660a7f626ac464619aa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867321"
---
# <span data-ttu-id="c3485-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c3485-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="c3485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3485-102">SYNOPSIS</span></span>
<span data-ttu-id="c3485-103">기록 된 범주와 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="c3485-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3485-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3485-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c3485-105">DESCRIPTION</span></span>
<span data-ttu-id="c3485-106">**AzDiagnosticSetting** cmdlet은 리소스에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="c3485-107">시간 세분화는 메트릭의 집계 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="c3485-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c3485-108">EXAMPLES</span></span>

### <span data-ttu-id="c3485-109">예제 1: 로깅 범주 및 시간 grains의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3485-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="c3485-110">이 명령은/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.의 *ResourceId* 로 Azure Key Vault에 대해 기록 되는 범주 및 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="c3485-111">변수</span><span class="sxs-lookup"><span data-stu-id="c3485-111">PARAMETERS</span></span>

### <span data-ttu-id="c3485-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3485-112">-DefaultProfile</span></span>
<span data-ttu-id="c3485-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c3485-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3485-114">-이름</span><span class="sxs-lookup"><span data-stu-id="c3485-114">-Name</span></span>
<span data-ttu-id="c3485-115">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="c3485-116">이전 API에 나와 있는 것 처럼 통화를 기본적으로 "서비스"로 지정 하지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="c3485-116">If not given the call default to "service" as it was in the previous API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3485-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3485-117">-ResourceId</span></span>
<span data-ttu-id="c3485-118">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="c3485-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3485-119">CommonParameters</span></span>
<span data-ttu-id="c3485-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3485-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3485-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3485-122">입력</span><span class="sxs-lookup"><span data-stu-id="c3485-122">INPUTS</span></span>

### <span data-ttu-id="c3485-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3485-123">System.String</span></span>

## <span data-ttu-id="c3485-124">출력</span><span class="sxs-lookup"><span data-stu-id="c3485-124">OUTPUTS</span></span>

### <span data-ttu-id="c3485-125">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3485-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="c3485-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c3485-126">NOTES</span></span>

## <span data-ttu-id="c3485-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3485-127">RELATED LINKS</span></span>

<span data-ttu-id="c3485-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [제거-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="c3485-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
