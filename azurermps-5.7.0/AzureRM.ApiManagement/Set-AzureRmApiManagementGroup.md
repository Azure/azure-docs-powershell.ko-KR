---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530581"
---
# <span data-ttu-id="57b73-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="57b73-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="57b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b73-102">SYNOPSIS</span></span>
<span data-ttu-id="57b73-103">API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57b73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57b73-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b73-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57b73-105">DESCRIPTION</span></span>
<span data-ttu-id="57b73-106">**AzureRmApiManagementGroup** CMDLET은 API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="57b73-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57b73-107">EXAMPLES</span></span>

### <span data-ttu-id="57b73-108">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="57b73-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="57b73-109">이 명령은 Group0001 이라는 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="57b73-110">변수</span><span class="sxs-lookup"><span data-stu-id="57b73-110">PARAMETERS</span></span>

### <span data-ttu-id="57b73-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="57b73-111">-Context</span></span>
<span data-ttu-id="57b73-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b73-113">-DefaultProfile</span></span>
<span data-ttu-id="57b73-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="57b73-115">-설명</span><span class="sxs-lookup"><span data-stu-id="57b73-115">-Description</span></span>
<span data-ttu-id="57b73-116">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b73-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="57b73-117">-GroupId</span></span>
<span data-ttu-id="57b73-118">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b73-119">-이름</span><span class="sxs-lookup"><span data-stu-id="57b73-119">-Name</span></span>
<span data-ttu-id="57b73-120">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b73-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57b73-121">-PassThru</span></span>
<span data-ttu-id="57b73-122">passthru</span><span class="sxs-lookup"><span data-stu-id="57b73-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57b73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b73-123">CommonParameters</span></span>
<span data-ttu-id="57b73-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b73-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b73-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b73-126">입력</span><span class="sxs-lookup"><span data-stu-id="57b73-126">INPUTS</span></span>

### <span data-ttu-id="57b73-127">않아야</span><span class="sxs-lookup"><span data-stu-id="57b73-127">None</span></span>
<span data-ttu-id="57b73-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57b73-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57b73-129">출력</span><span class="sxs-lookup"><span data-stu-id="57b73-129">OUTPUTS</span></span>

### <span data-ttu-id="57b73-130">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="57b73-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="57b73-131">상속자</span><span class="sxs-lookup"><span data-stu-id="57b73-131">NOTES</span></span>

## <span data-ttu-id="57b73-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57b73-132">RELATED LINKS</span></span>

[<span data-ttu-id="57b73-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="57b73-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="57b73-134">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="57b73-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="57b73-135">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="57b73-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


