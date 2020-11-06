---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: fb55eec3dc0bf3cf83032251e017749a07970f2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525823"
---
# <span data-ttu-id="55dc6-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="55dc6-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="55dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="55dc6-103">Analysis Services 서버 인스턴스 삭제</span><span class="sxs-lookup"><span data-stu-id="55dc6-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55dc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55dc6-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55dc6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="55dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="55dc6-106">Remove-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="55dc6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="55dc6-107">EXAMPLES</span></span>

### <span data-ttu-id="55dc6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="55dc6-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="55dc6-109">이 명령은 resourcegroup testserver에서 testserver 라는 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="55dc6-110">변수</span><span class="sxs-lookup"><span data-stu-id="55dc6-110">PARAMETERS</span></span>

### <span data-ttu-id="55dc6-111">-이름</span><span class="sxs-lookup"><span data-stu-id="55dc6-111">-Name</span></span>
<span data-ttu-id="55dc6-112">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="55dc6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55dc6-113">-PassThru</span></span>
<span data-ttu-id="55dc6-114">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="55dc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55dc6-115">-ResourceGroupName</span></span>
<span data-ttu-id="55dc6-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="55dc6-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="55dc6-117">-확인</span><span class="sxs-lookup"><span data-stu-id="55dc6-117">-Confirm</span></span>
<span data-ttu-id="55dc6-118">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="55dc6-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="55dc6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55dc6-119">-WhatIf</span></span>
<span data-ttu-id="55dc6-120">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="55dc6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dc6-121">-DefaultProfile</span></span>
<span data-ttu-id="55dc6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55dc6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dc6-123">CommonParameters</span></span>
<span data-ttu-id="55dc6-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55dc6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dc6-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55dc6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dc6-126">입력</span><span class="sxs-lookup"><span data-stu-id="55dc6-126">INPUTS</span></span>

## <span data-ttu-id="55dc6-127">출력</span><span class="sxs-lookup"><span data-stu-id="55dc6-127">OUTPUTS</span></span>

### <span data-ttu-id="55dc6-128">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="55dc6-128">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="55dc6-129">상속자</span><span class="sxs-lookup"><span data-stu-id="55dc6-129">NOTES</span></span>
<span data-ttu-id="55dc6-130">별칭: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="55dc6-130">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="55dc6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55dc6-131">RELATED LINKS</span></span>

[<span data-ttu-id="55dc6-132">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="55dc6-132">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="55dc6-133">새로운 AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="55dc6-133">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
