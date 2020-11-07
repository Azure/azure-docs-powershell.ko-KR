---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703289"
---
# <span data-ttu-id="365f3-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="365f3-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="365f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365f3-102">SYNOPSIS</span></span>
<span data-ttu-id="365f3-103">Analysis Services 서버 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="365f3-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="365f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="365f3-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="365f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="365f3-105">DESCRIPTION</span></span>
<span data-ttu-id="365f3-106">Resume-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="365f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="365f3-107">EXAMPLES</span></span>

### <span data-ttu-id="365f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="365f3-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="365f3-109">이 명령은 resourcegroup testserver에서 이름이 지정 된 서버를 일시 중지 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="365f3-110">변수</span><span class="sxs-lookup"><span data-stu-id="365f3-110">PARAMETERS</span></span>

### <span data-ttu-id="365f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365f3-111">-DefaultProfile</span></span>
<span data-ttu-id="365f3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="365f3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="365f3-113">-Name</span></span>
<span data-ttu-id="365f3-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="365f3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="365f3-115">-PassThru</span></span>
<span data-ttu-id="365f3-116">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="365f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="365f3-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="365f3-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365f3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="365f3-119">-Confirm</span></span>
<span data-ttu-id="365f3-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="365f3-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365f3-121">-WhatIf</span></span>
<span data-ttu-id="365f3-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365f3-123">CommonParameters</span></span>
<span data-ttu-id="365f3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365f3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365f3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365f3-126">입력</span><span class="sxs-lookup"><span data-stu-id="365f3-126">INPUTS</span></span>

### <span data-ttu-id="365f3-127">않아야</span><span class="sxs-lookup"><span data-stu-id="365f3-127">None</span></span>
<span data-ttu-id="365f3-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="365f3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="365f3-129">출력</span><span class="sxs-lookup"><span data-stu-id="365f3-129">OUTPUTS</span></span>

### <span data-ttu-id="365f3-130">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="365f3-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="365f3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="365f3-131">NOTES</span></span>
<span data-ttu-id="365f3-132">별칭: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="365f3-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="365f3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="365f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="365f3-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="365f3-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="365f3-135">일시 중단-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="365f3-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
