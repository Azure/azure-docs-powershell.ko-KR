---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046571"
---
# <span data-ttu-id="dbd35-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="dbd35-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="dbd35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd35-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd35-103">Azure RemoteApp 컬렉션의 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dbd35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbd35-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dbd35-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbd35-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd35-106">**AzureRemoteAppVM** cmdlet은 세션 호스팅을 위해 Azure RemoteApp 컬렉션에서 만든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="dbd35-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbd35-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd35-108">예제 1: 컬렉션에 가상 컴퓨터 표시</span><span class="sxs-lookup"><span data-stu-id="dbd35-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="dbd35-109">이 명령은 Contoso 라는 Azure RemoteApp 컬렉션에서 세션 호스팅에 사용 되는 가상 컴퓨터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="dbd35-110">변수</span><span class="sxs-lookup"><span data-stu-id="dbd35-110">PARAMETERS</span></span>

### <span data-ttu-id="dbd35-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="dbd35-111">-CollectionName</span></span>
<span data-ttu-id="dbd35-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="dbd35-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="dbd35-113">-Profile</span></span>
<span data-ttu-id="dbd35-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dbd35-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dbd35-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd35-116">CommonParameters</span></span>
<span data-ttu-id="dbd35-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd35-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd35-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd35-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd35-119">입력</span><span class="sxs-lookup"><span data-stu-id="dbd35-119">INPUTS</span></span>

## <span data-ttu-id="dbd35-120">출력</span><span class="sxs-lookup"><span data-stu-id="dbd35-120">OUTPUTS</span></span>

## <span data-ttu-id="dbd35-121">상속자</span><span class="sxs-lookup"><span data-stu-id="dbd35-121">NOTES</span></span>

## <span data-ttu-id="dbd35-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbd35-122">RELATED LINKS</span></span>

[<span data-ttu-id="dbd35-123">다시 시작-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="dbd35-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


