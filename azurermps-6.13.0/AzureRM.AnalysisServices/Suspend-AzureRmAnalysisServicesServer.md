---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703517"
---
# <span data-ttu-id="feb8d-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="feb8d-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="feb8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="feb8d-103">Analysis Services 서버 인스턴스 일시 중단</span><span class="sxs-lookup"><span data-stu-id="feb8d-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feb8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feb8d-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb8d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="feb8d-105">DESCRIPTION</span></span>
<span data-ttu-id="feb8d-106">Suspend-AzureRmAnalysisServicesServer cmdlet이 Analysis Services 서버 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="feb8d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="feb8d-107">EXAMPLES</span></span>

### <span data-ttu-id="feb8d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="feb8d-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="feb8d-109">이 명령은 resourcegroup testserver에서 testserver 라는 활성 서버를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="feb8d-110">변수</span><span class="sxs-lookup"><span data-stu-id="feb8d-110">PARAMETERS</span></span>

### <span data-ttu-id="feb8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb8d-111">-DefaultProfile</span></span>
<span data-ttu-id="feb8d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb8d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="feb8d-113">-Name</span></span>
<span data-ttu-id="feb8d-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="feb8d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="feb8d-115">-PassThru</span></span>
<span data-ttu-id="feb8d-116">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="feb8d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb8d-117">-ResourceGroupName</span></span>
<span data-ttu-id="feb8d-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="feb8d-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb8d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="feb8d-119">-Confirm</span></span>
<span data-ttu-id="feb8d-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="feb8d-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="feb8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb8d-121">-WhatIf</span></span>
<span data-ttu-id="feb8d-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="feb8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb8d-123">CommonParameters</span></span>
<span data-ttu-id="feb8d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feb8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb8d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb8d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb8d-126">입력</span><span class="sxs-lookup"><span data-stu-id="feb8d-126">INPUTS</span></span>

### <span data-ttu-id="feb8d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="feb8d-127">System.String</span></span>

## <span data-ttu-id="feb8d-128">출력</span><span class="sxs-lookup"><span data-stu-id="feb8d-128">OUTPUTS</span></span>

### <span data-ttu-id="feb8d-129">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="feb8d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="feb8d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="feb8d-130">NOTES</span></span>
<span data-ttu-id="feb8d-131">별칭: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="feb8d-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="feb8d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feb8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="feb8d-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="feb8d-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="feb8d-134">이력서-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="feb8d-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

