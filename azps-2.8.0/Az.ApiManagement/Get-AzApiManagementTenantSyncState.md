---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: c8d3ff0d268c4a84269585af7e769b46af663f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698085"
---
# <span data-ttu-id="9ba5f-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="9ba5f-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="9ba5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba5f-103">구성 데이터베이스와 Git 리포지토리 간의 최근 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9ba5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba5f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba5f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba5f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba5f-106">**AzApiManagementTenantSyncState** cmdlet은 구성 데이터베이스와 Git 리포지토리 간의 최신 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9ba5f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba5f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba5f-108">예제 1: 최신 동기화 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ba5f-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="9ba5f-109">이 명령은 구성 데이터베이스와 Git 리포지토리 간에 가장 최근의 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="9ba5f-110">변수</span><span class="sxs-lookup"><span data-stu-id="9ba5f-110">PARAMETERS</span></span>

### <span data-ttu-id="9ba5f-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9ba5f-111">-Context</span></span>
<span data-ttu-id="9ba5f-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba5f-113">-DefaultProfile</span></span>
<span data-ttu-id="9ba5f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba5f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba5f-115">CommonParameters</span></span>
<span data-ttu-id="9ba5f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba5f-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ba5f-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba5f-118">입력</span><span class="sxs-lookup"><span data-stu-id="9ba5f-118">INPUTS</span></span>

### <span data-ttu-id="9ba5f-119">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ba5f-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9ba5f-120">출력</span><span class="sxs-lookup"><span data-stu-id="9ba5f-120">OUTPUTS</span></span>

### <span data-ttu-id="9ba5f-121">ApiManagement. ServiceManagement. \ PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="9ba5f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="9ba5f-122">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba5f-122">NOTES</span></span>

## <span data-ttu-id="9ba5f-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba5f-123">RELATED LINKS</span></span>
