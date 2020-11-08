---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046235"
---
# <span data-ttu-id="4d734-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4d734-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="4d734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d734-102">SYNOPSIS</span></span>
<span data-ttu-id="4d734-103">빈 ACL 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="4d734-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d734-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4d734-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4d734-105">DESCRIPTION</span></span>
<span data-ttu-id="4d734-106">**새-AzureAclConfig** cmdlet은 빈 ACL (액세스 제어 목록) 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="4d734-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4d734-107">EXAMPLES</span></span>

### <span data-ttu-id="4d734-108">예제 1: ACL 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4d734-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="4d734-109">이 명령은 빈 ACL 구성 개체를 만든 다음 $Acl 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="4d734-110">변수</span><span class="sxs-lookup"><span data-stu-id="4d734-110">PARAMETERS</span></span>

### <span data-ttu-id="4d734-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4d734-111">-InformationAction</span></span>
<span data-ttu-id="4d734-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4d734-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d734-114">하기로</span><span class="sxs-lookup"><span data-stu-id="4d734-114">Continue</span></span>
- <span data-ttu-id="4d734-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="4d734-115">Ignore</span></span>
- <span data-ttu-id="4d734-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="4d734-116">Inquire</span></span>
- <span data-ttu-id="4d734-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4d734-117">SilentlyContinue</span></span>
- <span data-ttu-id="4d734-118">중지가</span><span class="sxs-lookup"><span data-stu-id="4d734-118">Stop</span></span>
- <span data-ttu-id="4d734-119">대기</span><span class="sxs-lookup"><span data-stu-id="4d734-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d734-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4d734-120">-InformationVariable</span></span>
<span data-ttu-id="4d734-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d734-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d734-122">CommonParameters</span></span>
<span data-ttu-id="4d734-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d734-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d734-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d734-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d734-125">입력</span><span class="sxs-lookup"><span data-stu-id="4d734-125">INPUTS</span></span>

## <span data-ttu-id="4d734-126">출력</span><span class="sxs-lookup"><span data-stu-id="4d734-126">OUTPUTS</span></span>

## <span data-ttu-id="4d734-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4d734-127">NOTES</span></span>

## <span data-ttu-id="4d734-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d734-128">RELATED LINKS</span></span>

[<span data-ttu-id="4d734-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4d734-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="4d734-130">-AzureAclConfig 제거</span><span class="sxs-lookup"><span data-stu-id="4d734-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="4d734-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4d734-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


