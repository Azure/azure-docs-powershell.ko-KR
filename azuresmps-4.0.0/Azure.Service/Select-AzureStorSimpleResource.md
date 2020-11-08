---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045448"
---
# <span data-ttu-id="9b20b-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="9b20b-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="9b20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b20b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b20b-103">자원을 현재 자원으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="9b20b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b20b-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b20b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b20b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b20b-106">**선택-AzureStorSimpleResource** cmdlet은 리소스를 현재 리소스로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="9b20b-107">리소스를 선택 하면 다른 cmdlet이 해당 리소스 컨텍스트 내에서 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="9b20b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9b20b-108">EXAMPLES</span></span>

### <span data-ttu-id="9b20b-109">예제 1: 처음으로 자원 선택</span><span class="sxs-lookup"><span data-stu-id="9b20b-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="9b20b-110">이 명령은 Contoso64-Tsqa 이라는 리소스를 현재 컨텍스트로 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="9b20b-111">이 예제에서는 이전에 컴퓨터에이 컨텍스트가 초기화 되지 않았으므로 *Registrationkey* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="9b20b-112">예제 2: 리소스 선택 시도</span><span class="sxs-lookup"><span data-stu-id="9b20b-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="9b20b-113">예제 3: 이전에 선택한 리소스 선택</span><span class="sxs-lookup"><span data-stu-id="9b20b-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="9b20b-114">이 명령은 Contoso64-Tsqa 이라는 리소스를 현재 컨텍스트로 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="9b20b-115">이 예제에서는 해당 컨텍스트가 이전에 선택 되어 있으므로 *Registrationkey* 매개 변수에 대 한 값을 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="9b20b-116">변수</span><span class="sxs-lookup"><span data-stu-id="9b20b-116">PARAMETERS</span></span>

### <span data-ttu-id="9b20b-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="9b20b-117">-Profile</span></span>
<span data-ttu-id="9b20b-118">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-118">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b20b-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="9b20b-119">-RegistrationKey</span></span>
<span data-ttu-id="9b20b-120">등록 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-120">Specifies a registration key.</span></span>
<span data-ttu-id="9b20b-121">자원을 처음 선택할 때 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="9b20b-122">이 cmdlet은 현재 리소스를 선택 하면 필요에 따라 cmdlet에서이 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="9b20b-123">자세한 내용은 Microsoft 개발자 네트워크에서 [서비스 등록 키 가져오기를](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  참조 하세요 https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9b20b-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="9b20b-124">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="9b20b-124">-ResourceName</span></span>
<span data-ttu-id="9b20b-125">현재 자원으로 선택할 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-125">Specifies the name of the resource to select as the current resource.</span></span>

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

### <span data-ttu-id="9b20b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b20b-126">CommonParameters</span></span>
<span data-ttu-id="9b20b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b20b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b20b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b20b-129">입력</span><span class="sxs-lookup"><span data-stu-id="9b20b-129">INPUTS</span></span>

### <span data-ttu-id="9b20b-130">않아야</span><span class="sxs-lookup"><span data-stu-id="9b20b-130">None</span></span>

## <span data-ttu-id="9b20b-131">출력</span><span class="sxs-lookup"><span data-stu-id="9b20b-131">OUTPUTS</span></span>

### <span data-ttu-id="9b20b-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="9b20b-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="9b20b-133">이 cmdlet은 리소스 컨텍스트에 대 한 세부 정보를 포함 하는 **StorSimpleResourceContext** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b20b-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="9b20b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9b20b-134">NOTES</span></span>

## <span data-ttu-id="9b20b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b20b-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b20b-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="9b20b-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="9b20b-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="9b20b-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


