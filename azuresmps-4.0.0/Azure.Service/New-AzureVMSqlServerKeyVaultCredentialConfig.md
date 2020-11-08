---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046188"
---
# <span data-ttu-id="2a291-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="2a291-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="2a291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a291-102">SYNOPSIS</span></span>

## <span data-ttu-id="2a291-103">구문과</span><span class="sxs-lookup"><span data-stu-id="2a291-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a291-104">설명은</span><span class="sxs-lookup"><span data-stu-id="2a291-104">DESCRIPTION</span></span>

## <span data-ttu-id="2a291-105">예제의</span><span class="sxs-lookup"><span data-stu-id="2a291-105">EXAMPLES</span></span>

### <span data-ttu-id="2a291-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="2a291-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2a291-107">변수</span><span class="sxs-lookup"><span data-stu-id="2a291-107">PARAMETERS</span></span>

### <span data-ttu-id="2a291-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2a291-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a291-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2a291-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a291-110">-사용</span><span class="sxs-lookup"><span data-stu-id="2a291-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a291-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2a291-111">-InformationAction</span></span>
<span data-ttu-id="2a291-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a291-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2a291-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2a291-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a291-114">하기로</span><span class="sxs-lookup"><span data-stu-id="2a291-114">Continue</span></span>
- <span data-ttu-id="2a291-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="2a291-115">Ignore</span></span>
- <span data-ttu-id="2a291-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="2a291-116">Inquire</span></span>
- <span data-ttu-id="2a291-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2a291-117">SilentlyContinue</span></span>
- <span data-ttu-id="2a291-118">중지가</span><span class="sxs-lookup"><span data-stu-id="2a291-118">Stop</span></span>
- <span data-ttu-id="2a291-119">대기</span><span class="sxs-lookup"><span data-stu-id="2a291-119">Suspend</span></span>

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

### <span data-ttu-id="2a291-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2a291-120">-InformationVariable</span></span>
<span data-ttu-id="2a291-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a291-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2a291-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="2a291-122">-Profile</span></span>
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

### <span data-ttu-id="2a291-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a291-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a291-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="2a291-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a291-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a291-125">CommonParameters</span></span>
<span data-ttu-id="2a291-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a291-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a291-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a291-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a291-128">입력</span><span class="sxs-lookup"><span data-stu-id="2a291-128">INPUTS</span></span>

## <span data-ttu-id="2a291-129">출력</span><span class="sxs-lookup"><span data-stu-id="2a291-129">OUTPUTS</span></span>

## <span data-ttu-id="2a291-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2a291-130">NOTES</span></span>

## <span data-ttu-id="2a291-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a291-131">RELATED LINKS</span></span>

