---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528167"
---
# <span data-ttu-id="d8405-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="d8405-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="d8405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8405-102">SYNOPSIS</span></span>
<span data-ttu-id="d8405-103">Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 Analysis Services 서버 인스턴스에서 로그를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d8405-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8405-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8405-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="d8405-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8405-105">DESCRIPTION</span></span>
<span data-ttu-id="d8405-106">Export-AzureAnalysisServicesInstance cmdlet은 Azure Analysis Services 서버 인스턴스에서 로그를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d8405-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="d8405-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8405-107">EXAMPLES</span></span>

### <span data-ttu-id="d8405-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8405-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="d8405-109">이 명령은 Add-AzureAnalysisServicesAccount 명령에 지정 된 환경의 ' testserver ' 서버에서 로그를 내보내고 OutputPath ' C:\path\to\log\testserver.log '에 지정 된 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8405-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="d8405-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8405-110">PARAMETERS</span></span>

### <span data-ttu-id="d8405-111">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="d8405-111">-Instance</span></span>
<span data-ttu-id="d8405-112">Analysis Services 서버 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8405-112">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="d8405-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="d8405-113">-OutputPath</span></span>
<span data-ttu-id="d8405-114">내보낼 파일의 출력 경로 로그</span><span class="sxs-lookup"><span data-stu-id="d8405-114">Output path to file to export log</span></span>

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

### <span data-ttu-id="d8405-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d8405-115">-Force</span></span>
<span data-ttu-id="d8405-116">묻지 않고 파일이 있는 경우 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="d8405-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d8405-117">입력</span><span class="sxs-lookup"><span data-stu-id="d8405-117">INPUTS</span></span>

### <span data-ttu-id="d8405-118">않아야</span><span class="sxs-lookup"><span data-stu-id="d8405-118">None</span></span>
<span data-ttu-id="d8405-119">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8405-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8405-120">출력</span><span class="sxs-lookup"><span data-stu-id="d8405-120">OUTPUTS</span></span>

## <span data-ttu-id="d8405-121">상속자</span><span class="sxs-lookup"><span data-stu-id="d8405-121">NOTES</span></span>
<span data-ttu-id="d8405-122">별칭: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d8405-122">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="d8405-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8405-123">RELATED LINKS</span></span>
