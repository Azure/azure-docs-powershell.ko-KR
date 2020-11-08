---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045703"
---
# <span data-ttu-id="8722f-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="8722f-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="8722f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8722f-102">SYNOPSIS</span></span>
<span data-ttu-id="8722f-103">Azure Active Directory에서 더 이상 존재 하지 않는 Azure RemoteApp 가상 컴퓨터와 연결 된 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="8722f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8722f-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8722f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8722f-105">DESCRIPTION</span></span>
<span data-ttu-id="8722f-106">**AzureRemoteAppVmStaleAdObject** cmdlet은 더 이상 존재 하지 않는 azure RemoteApp 가상 컴퓨터와 연결 된 Azure Active Directory의 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="8722f-107">Azure Active Directory 개체를 제거할 권한이 있는 자격 증명을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="8722f-108">*Verbose* 공용 매개 변수를 지정 하면이 cmdlet은 삭제 하는 각 개체의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="8722f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8722f-109">EXAMPLES</span></span>

### <span data-ttu-id="8722f-110">예제 1: 컬렉션에 대 한 부실 개체 지우기</span><span class="sxs-lookup"><span data-stu-id="8722f-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="8722f-111">첫 번째 명령은 **Get-Credential** 을 사용 하 여 사용자 이름과 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="8722f-112">명령이 $AdminCredentials 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="8722f-113">두 번째 명령은 Contoso 라는 컬렉션에 대 한 부실 개체를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="8722f-114">이 명령은 $AdminCredentials 변수에 저장 된 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="8722f-115">명령이 제대로 수행 되려면 해당 자격 증명에 적절 한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="8722f-116">변수</span><span class="sxs-lookup"><span data-stu-id="8722f-116">PARAMETERS</span></span>

### <span data-ttu-id="8722f-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8722f-117">-CollectionName</span></span>
<span data-ttu-id="8722f-118">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8722f-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="8722f-119">-Credential</span></span>
<span data-ttu-id="8722f-120">이 작업을 수행할 수 있는 권한이 있는 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="8722f-121">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="8722f-122">이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 사용자 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8722f-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="8722f-123">-Profile</span></span>
<span data-ttu-id="8722f-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8722f-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8722f-126">-확인</span><span class="sxs-lookup"><span data-stu-id="8722f-126">-Confirm</span></span>
<span data-ttu-id="8722f-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8722f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8722f-128">-WhatIf</span></span>
<span data-ttu-id="8722f-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8722f-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8722f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8722f-131">CommonParameters</span></span>
<span data-ttu-id="8722f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8722f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8722f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8722f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8722f-134">입력</span><span class="sxs-lookup"><span data-stu-id="8722f-134">INPUTS</span></span>

## <span data-ttu-id="8722f-135">출력</span><span class="sxs-lookup"><span data-stu-id="8722f-135">OUTPUTS</span></span>

## <span data-ttu-id="8722f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8722f-136">NOTES</span></span>

## <span data-ttu-id="8722f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8722f-137">RELATED LINKS</span></span>

[<span data-ttu-id="8722f-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="8722f-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


