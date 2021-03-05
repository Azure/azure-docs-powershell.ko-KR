---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980064"
---
# <span data-ttu-id="82922-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="82922-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="82922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82922-102">SYNOPSIS</span></span>
<span data-ttu-id="82922-103">기록된 범주 및 시간 입자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82922-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="82922-104">구문</span><span class="sxs-lookup"><span data-stu-id="82922-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82922-105">설명</span><span class="sxs-lookup"><span data-stu-id="82922-105">DESCRIPTION</span></span>
<span data-ttu-id="82922-106">**Get-AzDiagnosticSetting** cmdlet은 리소스에 대해 기록된 범주 및 시간 그레인을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82922-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="82922-107">시간 그레인은 메트릭의 집계 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="82922-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="82922-108">예제</span><span class="sxs-lookup"><span data-stu-id="82922-108">EXAMPLES</span></span>

### <span data-ttu-id="82922-109">예제 1: 로깅 범주 및 시간 입자의 상태 확인</span><span class="sxs-lookup"><span data-stu-id="82922-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="82922-110">이 명령은 /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault를 사용하여 Azure Key Vault에 기록된 범주 및 시간 그레인을 얻습니다. </span><span class="sxs-lookup"><span data-stu-id="82922-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="82922-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="82922-111">PARAMETERS</span></span>

### <span data-ttu-id="82922-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82922-112">-DefaultProfile</span></span>
<span data-ttu-id="82922-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82922-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82922-114">-Name</span><span class="sxs-lookup"><span data-stu-id="82922-114">-Name</span></span>
<span data-ttu-id="82922-115">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82922-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="82922-116">이전 API에서와 같은 호출 기본값을 "service"로 지정하지 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="82922-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="82922-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82922-117">-ResourceId</span></span>
<span data-ttu-id="82922-118">리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82922-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="82922-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82922-119">CommonParameters</span></span>
<span data-ttu-id="82922-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82922-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82922-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82922-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82922-122">입력</span><span class="sxs-lookup"><span data-stu-id="82922-122">INPUTS</span></span>

### <span data-ttu-id="82922-123">System.String</span><span class="sxs-lookup"><span data-stu-id="82922-123">System.String</span></span>

## <span data-ttu-id="82922-124">출력</span><span class="sxs-lookup"><span data-stu-id="82922-124">OUTPUTS</span></span>

### <span data-ttu-id="82922-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="82922-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="82922-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82922-126">NOTES</span></span>

## <span data-ttu-id="82922-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82922-127">RELATED LINKS</span></span>

<span data-ttu-id="82922-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="82922-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
