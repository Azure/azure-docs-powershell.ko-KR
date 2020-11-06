---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535523"
---
# <span data-ttu-id="ecf09-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecf09-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="ecf09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf09-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf09-103">API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecf09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecf09-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecf09-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf09-106">**AzureRmApiManagementGroup** CMDLET은 API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="ecf09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecf09-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf09-108">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="ecf09-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="ecf09-109">이 명령은 Group0001 이라는 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="ecf09-110">변수</span><span class="sxs-lookup"><span data-stu-id="ecf09-110">PARAMETERS</span></span>

### <span data-ttu-id="ecf09-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecf09-111">-Context</span></span>
<span data-ttu-id="ecf09-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf09-113">-설명</span><span class="sxs-lookup"><span data-stu-id="ecf09-113">-Description</span></span>
<span data-ttu-id="ecf09-114">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="ecf09-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ecf09-115">-GroupId</span></span>
<span data-ttu-id="ecf09-116">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-116">Specifies the identifier of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf09-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ecf09-117">-Name</span></span>
<span data-ttu-id="ecf09-118">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="ecf09-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecf09-119">-PassThru</span></span>
<span data-ttu-id="ecf09-120">passthru</span><span class="sxs-lookup"><span data-stu-id="ecf09-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf09-121">-DefaultProfile</span></span>
<span data-ttu-id="ecf09-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf09-123">CommonParameters</span></span>
<span data-ttu-id="ecf09-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf09-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf09-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf09-126">입력</span><span class="sxs-lookup"><span data-stu-id="ecf09-126">INPUTS</span></span>

## <span data-ttu-id="ecf09-127">출력</span><span class="sxs-lookup"><span data-stu-id="ecf09-127">OUTPUTS</span></span>

### <span data-ttu-id="ecf09-128">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecf09-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="ecf09-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ecf09-129">NOTES</span></span>

## <span data-ttu-id="ecf09-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecf09-130">RELATED LINKS</span></span>

[<span data-ttu-id="ecf09-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecf09-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ecf09-132">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecf09-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ecf09-133">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ecf09-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


