---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528159"
---
# <span data-ttu-id="8b10c-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8b10c-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="8b10c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b10c-102">SYNOPSIS</span></span>

<span data-ttu-id="8b10c-103">지정 된 Analysis Services 서버 인스턴스에서 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 현재 로그인 된 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b10c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b10c-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="8b10c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b10c-105">DESCRIPTION</span></span>

<span data-ttu-id="8b10c-106">Sync-AzureAnalysisServicesInstance cmdlet은 지정 된 Analysis Services server 인스턴스의 지정 된 데이터베이스를 Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 모든 query scaleout instance로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8b10c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b10c-107">EXAMPLES</span></span>

### <span data-ttu-id="8b10c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b10c-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8b10c-109">이 명령은 사용자가 Add-AzureAnalysisServicesAccount 명령을 사용 하 여이 환경에 로그인 한 환경에서 ' contoso ' 라는 서버의 SalesOrders 데이터베이스를 동기화 합니다. westus.asazure.windows.net를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8b10c-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b10c-110">PARAMETERS</span></span>

### <span data-ttu-id="8b10c-111">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="8b10c-111">-Instance</span></span>

<span data-ttu-id="8b10c-112">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="8b10c-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b10c-113">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8b10c-113">-Database</span></span>

<span data-ttu-id="8b10c-114">동기화 할 데이터베이스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b10c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b10c-115">-PassThru</span></span>

<span data-ttu-id="8b10c-116">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8b10c-117">입력</span><span class="sxs-lookup"><span data-stu-id="8b10c-117">INPUTS</span></span>

### <span data-ttu-id="8b10c-118">않아야</span><span class="sxs-lookup"><span data-stu-id="8b10c-118">None</span></span>
<span data-ttu-id="8b10c-119">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b10c-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b10c-120">출력</span><span class="sxs-lookup"><span data-stu-id="8b10c-120">OUTPUTS</span></span>

### <span data-ttu-id="8b10c-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8b10c-121">System.Boolean</span></span>

## <span data-ttu-id="8b10c-122">상속자</span><span class="sxs-lookup"><span data-stu-id="8b10c-122">NOTES</span></span>

<span data-ttu-id="8b10c-123">별칭: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="8b10c-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="8b10c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b10c-124">RELATED LINKS</span></span>
