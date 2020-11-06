---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 496c0410808604303ab60d8ad4d989e838828bf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526463"
---
# <span data-ttu-id="02b9a-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="02b9a-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="02b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="02b9a-103">Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경에서 Analysis Services 서버 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02b9a-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance -Instance <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="02b9a-106">Restart-AzureAnalysisServicesInstance cmdlet이 Azure Analysis Services 서버의 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="02b9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="02b9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="02b9a-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="02b9a-109">이 명령을 실행 하면 Add-AzureAnalysisServicesAccount 명령에 지정 된 환경에서 서버 ' testserver '가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="02b9a-110">변수</span><span class="sxs-lookup"><span data-stu-id="02b9a-110">PARAMETERS</span></span>

### <span data-ttu-id="02b9a-111">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="02b9a-111">-Instance</span></span>
<span data-ttu-id="02b9a-112">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="02b9a-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02b9a-113">-PassThru</span></span>
<span data-ttu-id="02b9a-114">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9a-115">-확인</span><span class="sxs-lookup"><span data-stu-id="02b9a-115">-Confirm</span></span>
<span data-ttu-id="02b9a-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b9a-117">-WhatIf</span></span>
<span data-ttu-id="02b9a-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b9a-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b9a-120">CommonParameters</span></span>
<span data-ttu-id="02b9a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b9a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b9a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b9a-123">입력</span><span class="sxs-lookup"><span data-stu-id="02b9a-123">INPUTS</span></span>

### <span data-ttu-id="02b9a-124">않아야</span><span class="sxs-lookup"><span data-stu-id="02b9a-124">None</span></span>

## <span data-ttu-id="02b9a-125">출력</span><span class="sxs-lookup"><span data-stu-id="02b9a-125">OUTPUTS</span></span>

### <span data-ttu-id="02b9a-126">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="02b9a-126">System.Boolean</span></span>

## <span data-ttu-id="02b9a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="02b9a-127">NOTES</span></span>
<span data-ttu-id="02b9a-128">별칭: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="02b9a-128">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="02b9a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02b9a-129">RELATED LINKS</span></span>
